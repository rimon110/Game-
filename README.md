import { useState } from "react";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { Input } from "@/components/ui/input";
import { Dialog, DialogContent, DialogTrigger } from "@/components/ui/dialog";
import { Youtube } from "lucide-react";
import Image from "next/image";

export default function GameStar() {
  const [coins, setCoins] = useState(0);
  const [name, setName] = useState("");
  const [number, setNumber] = useState("");
  const [open, setOpen] = useState(false);

  const handleClick = () => {
    setCoins(coins + 1);
  };

  const handleSubmit = (e: React.FormEvent) => {
    e.preventDefault();
    setOpen(true);
  };

  return (
    <div className="min-h-screen bg-yellow-50 flex flex-col items-center justify-center p-4">
      <h1 className="text-4xl font-bold text-center mb-6">🎮 Game Star</h1>

      <a
        href="https://youtube.com/@mdrimon8289?si=ub0Lpnvq5Mb1LLC0"
        target="_blank"
        rel="noopener noreferrer"
        className="flex items-center gap-2 text-red-600 mb-4 underline"
      >
        <Youtube /> সাবস্ক্রাইব করো আমার ইউটিউব চ্যানেল
      </a>

      <Card className="w-full max-w-sm bg-white shadow-xl">
        <CardContent className="flex flex-col items-center p-4">
          <Image
            src="https://cdn-icons-png.flaticon.com/512/3468/3468379.png"
            alt="Game Star"
            width={100}
            height={100}
            className="mb-4"
          />

          <div className="flex flex-col items-center mb-4">
            <span className="text-lg font-semibold">কয়েন: {coins}</span>
            <Button className="mt-2" onClick={handleClick}>
              কয়েন নাও +1
            </Button>
          </div>

          <form onSubmit={handleSubmit} className="w-full flex flex-col gap-2">
            <Input
              placeholder="তোমার নাম"
              value={name}
              onChange={e => setName(e.target.value)}
              required
            />
            <Input
              placeholder="তোমার নাম্বার"
              value={number}
              onChange={e => setNumber(e.target.value)}
              required
            />

            <Dialog open={open} onOpenChange={setOpen}>
              <DialogTrigger asChild>
                <Button type="submit" className="w-full mt-2">
                  সাবমিট করো
                </Button>
              </DialogTrigger>
              <DialogContent>
                <div className="space-y-2">
                  <h2 className="text-xl font-bold text-center">তোমার তথ্য</h2>
                  <p>
                    <strong>নাম:</strong> {name}
                  </p>
                  <p>
                    <strong>নাম্বার:</strong> {number}
                  </p>
                  <p>
                    <strong>মোট কয়েন:</strong> {coins}
                  </p>
                  <Button className="w-full" onClick={() => setOpen(false)}>
                    বন্ধ করুন
                  </Button>
                </div>
              </DialogContent>
            </Dialog>
          </form>
        </CardContent>
      </Card>
    </div>
  );
}import { useState } from "react";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { Input } from "@/components/ui/input";
import { Dialog, DialogContent, DialogTrigger } from "@/components/ui/dialog";
import { Youtube } from "lucide-react";
import Image from "next/image";

export default function GameStar() {
  const [coins, setCoins] = useState(0);
  const [name, setName] = useState("");
  const [number, setNumber] = useState("");
  const [open, setOpen] = useState(false);

  const handleClick = () => {
    setCoins(coins + 1);
  };

  const handleSubmit = (e: React.FormEvent) => {
    e.preventDefault();
    setOpen(true);
  };

  return (
    <div className="min-h-screen bg-yellow-50 flex flex-col items-center justify-center p-4">
      <h1 className="text-4xl font-bold text-center mb-6">🎮 Game Star</h1>

      <a
        href="https://youtube.com/@mdrimon8289?si=ub0Lpnvq5Mb1LLC0"
        target="_blank"
        rel="noopener noreferrer"
        className="flex items-center gap-2 text-red-600 mb-4 underline"
      >
        <Youtube /> সাবস্ক্রাইব করো আমার ইউটিউব চ্যানেল
      </a>

      <Card className="w-full max-w-sm bg-white shadow-xl">
        <CardContent className="flex flex-col items-center p-4">
          <Image
            src="https://cdn-icons-png.flaticon.com/512/3468/3468379.png"
            alt="Game Star"
            width={100}
            height={100}
            className="mb-4"
          />

          <div className="flex flex-col items-center mb-4">
            <span className="text-lg font-semibold">কয়েন: {coins}</span>
            <Button className="mt-2" onClick={handleClick}>
              কয়েন নাও +1
            </Button>
          </div>

          <form onSubmit={handleSubmit} className="w-full flex flex-col gap-2">
            <Input
              placeholder="তোমার নাম"
              value={name}
              onChange={e => setName(e.target.value)}
              required
            />
            <Input
              placeholder="তোমার নাম্বার"
              value={number}
              onChange={e => setNumber(e.target.value)}
              required
            />

            <Dialog open={open} onOpenChange={setOpen}>
              <DialogTrigger asChild>
                <Button type="submit" className="w-full mt-2">
                  সাবমিট করো
                </Button>
              </DialogTrigger>
              <DialogContent>
                <div className="space-y-2">
                  <h2 className="text-xl font-bold text-center">তোমার তথ্য</h2>
                  <p>
                    <strong>নাম:</strong> {name}
                  </p>
                  <p>
                    <strong>নাম্বার:</strong> {number}
                  </p>
                  <p>
                    <strong>মোট কয়েন:</strong> {coins}
                  </p>
                  <Button className="w-full" onClick={() => setOpen(false)}>
                    বন্ধ করুন
                  </Button>
                </div>
              </DialogContent>
            </Dialog>
          </form>
        </CardContent>
      </Card>
    </div>
  );
}import { useState } from "react";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { Input } from "@/components/ui/input";
import { Dialog, DialogContent, DialogTrigger } from "@/components/ui/dialog";
import { Youtube } from "lucide-react";
import Image from "next/image";

export default function GameStar() {
  const [coins, setCoins] = useState(0);
  const [name, setName] = useState("");
  const [number, setNumber] = useState("");
  const [open, setOpen] = useState(false);

  const handleClick = () => {
    setCoins(coins + 1);
  };

  const handleSubmit = (e: React.FormEvent) => {
    e.preventDefault();
    setOpen(true);
  };

  return (
    <div className="min-h-screen bg-yellow-50 flex flex-col items-center justify-center p-4">
      <h1 className="text-4xl font-bold text-center mb-6">🎮 Game Star</h1>

      <a
        href="https://youtube.com/@mdrimon8289?si=ub0Lpnvq5Mb1LLC0"
        target="_blank"
        rel="noopener noreferrer"
        className="flex items-center gap-2 text-red-600 mb-4 underline"
      >
        <Youtube /> সাবস্ক্রাইব করো আমার ইউটিউব চ্যানেল
      </a>

      <Card className="w-full max-w-sm bg-white shadow-xl">
        <CardContent className="flex flex-col items-center p-4">
          <Image
            src="https://cdn-icons-png.flaticon.com/512/3468/3468379.png"
            alt="Game Star"
            width={100}
            height={100}
            className="mb-4"
          />

          <div className="flex flex-col items-center mb-4">
            <span className="text-lg font-semibold">কয়েন: {coins}</span>
            <Button className="mt-2" onClick={handleClick}>
              কয়েন নাও +1
            </Button>
          </div>

          <form onSubmit={handleSubmit} className="w-full flex flex-col gap-2">
            <Input
              placeholder="তোমার নাম"
              value={name}
              onChange={e => setName(e.target.value)}
              required
            />
            <Input
              placeholder="তোমার নাম্বার"
              value={number}
              onChange={e => setNumber(e.target.value)}
              required
            />

            <Dialog open={open} onOpenChange={setOpen}>
              <DialogTrigger asChild>
                <Button type="submit" className="w-full mt-2">
                  সাবমিট করো
                </Button>
              </DialogTrigger>
              <DialogContent>
                <div className="space-y-2">
                  <h2 className="text-xl font-bold text-center">তোমার তথ্য</h2>
                  <p>
                    <strong>নাম:</strong> {name}
                  </p>
                  <p>
                    <strong>নাম্বার:</strong> {number}
                  </p>
                  <p>
                    <strong>মোট কয়েন:</strong> {coins}
                  </p>
                  <Button className="w-full" onClick={() => setOpen(false)}>
                    বন্ধ করুন
                  </Button>
                </div>
              </DialogContent>
            </Dialog>
          </form>
        </CardContent>
      </Card>
    </div>
  );
}![Screenshot_2025-01-17-08-17-58-20-01](https://github.com/user-attachments/assets/011018c3-fab2-4905-9e4f-9aa525f86968)
