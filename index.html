'use client';
import React, { useState } from 'react';

// Dữ liệu danh mục Charm (Bạn có thể thay hình ảnh và giá thực tế của shop)
const CHARM_CATEGORIES = [
  {
    category: "Chữ Cái",
    items: [
      { id: "charm-a", name: "Charm Chữ A", price: 35000, image: "https://via.placeholder.com/100/FFB6C1/000000?text=A" },
      { id: "charm-b", name: "Charm Chữ B", price: 35000, image: "https://via.placeholder.com/100/FFB6C1/000000?text=B" },
    ]
  },
  {
    category: "Biểu Tượng",
    items: [
      { id: "charm-heart", name: "Trái Tim Hồng", price: 45000, image: "https://via.placeholder.com/100/FFC0CB/000000?text=♥" },
      { id: "charm-star", name: "Ngôi Sao Vàng", price: 40000, image: "https://via.placeholder.com/100/FFFACD/000000?text=★" },
    ]
  }
];

// Danh sách dây đeo
const BRACELETS = [
  { id: "b1", name: "Vòng Xích Bạc Basic", price: 180000, image: "https://via.placeholder.com/400/F0F0F0/000000?text=Vong+Xich+Bac" }
];

export default function PunPunStyleCharmApp() {
  const [selectedBracelet, setSelectedBracelet] = useState(BRACELETS[0]);
  const [activeTab, setActiveTab] = useState(CHARM_CATEGORIES[0].category);
  
  // 5 vị trí đính charm trên chiếc vòng
  const [slots, setSlots] = useState([null, null, null, null, null]);
  const [activeSlot, setActiveSlot] = useState(0); // Vị trí đang chọn để gắn charm

  // SĐT Zalo nhận đơn của bạn
  const ZALO_PHONE = "0901234567"; 

  // Chọn charm cho vị trí đang active
  const handleSelectCharm = (charm) => {
    const newSlots = [...slots];
    newSlots[activeSlot] = charm;
    setSlots(newSlots);
    // Tự động chuyển sang nốt tiếp theo nếu chưa hết nốt
    if (activeSlot < slots.length - 1) {
      setActiveSlot(activeSlot + 1);
    }
  };

  // Gỡ charm tại vị trí
  const handleRemoveCharm = (index, e) => {
    e.stopPropagation();
    const newSlots = [...slots];
    newSlots[index] = null;
    setSlots(newSlots);
  };

  // Tính tổng tiền
  const totalCharmPrice = slots.reduce((acc, item) => acc + (item ? item.price : 0), 0);
  const grandTotal = selectedBracelet.price + totalCharmPrice;

  // Gửi đơn qua Zalo
  const handleOrder = () => {
    let msg = `✨ ĐƠN HÀNG THIẾT KẾ CHARM VỪA TẠO ✨\n`;
    msg += `--------------------------\n`;
    msg += `1. Loại dây: ${selectedBracelet.name} (${selectedBracelet.price.toLocaleString()}đ)\n`;
    msg += `2. Danh sách Charm đính kèm:\n`;
    
    let hasCharm = false;
    slots.forEach((item, idx) => {
      if (item) {
        hasCharm = true;
        msg += `   • Vị trí ${idx + 1}: ${item.name} (${item.price.toLocaleString()}đ)\n`;
      }
    });
    if (!hasCharm) msg += `   (Chưa chọn charm nào)\n`;
    
    msg += `--------------------------\n`;
    msg += `💰 TỔNG THÀNH TIỀN: ${grandTotal.toLocaleString()} VNĐ\n\n`;
    msg += `Shop tư vấn và chốt đơn cho mình nhé!`;

    window.open(`https://zalo.me/${ZALO_PHONE}?text=${encodeURIComponent(msg)}`, '_blank');
  };

  return (
    <div className="min-h-screen bg-[#FFF5F6] text-gray-700 flex flex-col font-sans max-w-md mx-auto shadow-2xl">
      {/* HEADER TÊN SHOP */}
      <header className="p-4 text-center bg-white border-b border-pink-100 sticky top-0 z-20">
        <h1 className="text-xl font-bold text-pink-500 tracking-wider">CHARM STUDIO</h1>
        <p className="text-xs text-gray-400">Tự tay thiết kế chiếc vòng của riêng bạn</p>
      </header>

      {/* KHUNG XEM THỬ VÒNG (PREVIEW CANVAS) */}
      <div className="p-4 flex flex-col items-center">
        <div className="relative w-72 h-72 bg-white rounded-3xl shadow-sm border border-pink-100 flex items-center justify-center overflow-hidden">
          {/* Ảnh chiếc vòng nền */}
          <img src={selectedBracelet.image} alt="Vòng" className="absolute w-full h-full object-contain pointer-events-none p-4" />

          {/* Hàng nút vị trí charm đính trên vòng */}
          <div className="absolute inset-0 flex items-center justify-center gap-2 px-6">
            {slots.map((charm, idx) => (
              <button
                key={idx}
                onClick={() => setActiveSlot(idx)}
                className={`w-11 h-11 rounded-full border-2 flex items-center justify-center transition-all relative ${
                  activeSlot === idx 
                    ? 'border-pink-500 bg-pink-50 scale-110 shadow-md ring-2 ring-pink-200' 
                    : 'border-dashed border-gray-300 bg-white/80'
                }`}
              >
                {charm ? (
                  <>
                    <img src={charm.image} alt={charm.name} className="w-8 h-8 object-contain" />
                    <span 
                      onClick={(e) => handleRemoveCharm(idx, e)}
                      className="absolute -top-1 -right-1 bg-red-400 text-white rounded-full w-4 h-4 text-[9px] flex items-center justify-center"
                    >
                      ✕
                    </span>
                  </>
                ) : (
                  <span className="text-[10px] text-gray-400 font-bold">{idx + 1}</span>
                )}
              </button>
            ))}
          </div>
        </div>

        <p className="text-xs text-gray-400 mt-2">
          Đang chọn gắn cho <span className="font-bold text-pink-500">Vị trí {activeSlot + 1}</span> (Chạm vào số để đổi vị trí)
        </p>
      </div>

      {/* MENU CHỌN CHARM (CATALOG) */}
      <div className="flex-1 bg-white rounded-t-3xl p-4 border-t border-pink-100 shadow-lg flex flex-col">
        {/* TAB DANH MỤC */}
        <div className="flex gap-2 border-b border-gray-100 pb-2 mb-3 overflow-x-auto no-scrollbar">
          {CHARM_CATEGORIES.map((cat) => (
            <button
              key={cat.category}
              onClick={() => setActiveTab(cat.category)}
              className={`px-4 py-1.5 rounded-full text-xs font-semibold whitespace-nowrap transition ${
                activeTab === cat.category 
                  ? 'bg-pink-500 text-white shadow-sm' 
                  : 'bg-gray-100 text-gray-500'
              }`}
            >
              {cat.category}
            </button>
          ))}
        </div>

        {/* DANH SÁCH CHARM THEO TAB */}
        <div className="grid grid-cols-4 gap-3 overflow-y-auto max-h-56 p-1">
          {CHARM_CATEGORIES.find(c => c.category === activeTab)?.items.map((charm) => (
            <button
              key={charm.id}
              onClick={() => handleSelectCharm(charm)}
              className="flex flex-col items-center bg-pink-50/40 p-2 rounded-xl border border-pink-100 hover:bg-pink-100 transition active:scale-95"
            >
              <img src={charm.image} alt={charm.name} className="w-10 h-10 object-contain mb-1" />
              <span className="text-[10px] font-medium text-gray-600 truncate w-full text-center">{charm.name}</span>
              <span className="text-[9px] text-pink-500 font-bold">{charm.price / 1000}k</span>
            </button>
          ))}
        </div>

        {/* THANH TỔNG TIỀN & NÚT CHỐT ĐƠN */}
        <div className="mt-auto pt-4 border-t border-gray-100 flex items-center justify-between">
          <div>
            <p className="text-[10px] text-gray-400 uppercase font-bold tracking-wider">Tổng tạm tính</p>
            <p className="text-lg font-extrabold text-pink-600">{grandTotal.toLocaleString()} đ</p>
          </div>
          <button
            onClick={handleOrder}
            className="bg-pink-500 text-white px-6 py-3 rounded-2xl font-bold text-sm shadow-lg shadow-pink-200 active:scale-95 transition"
          >
            Chốt Đơn Zalo 💬
          </button>
        </div>
      </div>
    </div>
  );
}
