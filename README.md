<span className="inline-block w-2.5 h-2.5 rounded-full bg-emerald-500 animate-pulse" />
            <span className="uppercase tracking-wider font-extrabold text-[10px] text-gray-450">
              {language === 'ckb' ? 'چالاکە ئێستا' : 'Live Gateway'}
            </span>
          </div>

          <p className="font-semibold text-gray-500">
            {profile.displayName} &copy; 2026 • {language === 'ckb' ? 'هەموو مافەکان پارێزراوە' : 'All Rights Reserved'}
          </p>
        </footer>
      </main>

      <AnimatePresence>
        {isAddOpen && (
          <AddChannelModal
            language={language}
            isOpen={isAddOpen}
            onClose={() => { setIsAddOpen(false); setEditingChannel(null); }}
            onSave={handleSaveChannel}
            editingChannel={editingChannel}
            categories={initialCategories}
          />
        )}
      </AnimatePresence>

      <AnimatePresence>
        {isProfileOpen && (
          <EditProfileModal
            language={language}
            isOpen={isProfileOpen}
            onClose={() => setIsProfileOpen(false)}
            onSave={handleSaveProfile}
            currentProfile={profile}
          />
        )}
      </AnimatePresence>
    </div>
  );
}

import { Channel, CreatorProfile, Category } from '../types';
import shazaLogo from '../assets/images/shaza_vip_logo_1780588907015.png';
import shazaCover from '../assets/images/shaza_vip_cover_1780588929185.png';

export const initialCategories: Category[] = [
  { id: 'all', labelEn: 'All Hubs', labelCkb: 'هەموو بەستەرەکان' },
  { id: 'gaming', labelEn: 'Gaming & Streams', labelCkb: 'چەناڵی هاک' },
  { id: 'chat', labelEn: 'Chat & Community', labelCkb: 'گروپ چات' },
  { id: 'key', labelEn: 'Keys & Licenses', labelCkb: 'کلیل' },
  { id: 'tutorial', labelEn: 'Tutorials', labelCkb: 'فێرکاری' },
  { id: 'official', labelEn: 'Official Account', labelCkb: 'ئەکاونتی فەرمی' }
];

export const initialProfile: CreatorProfile = {
  displayName: "SHAZA VIP",
  username: "Hamokal4ri",
  bio: " هەموو چەناڵەکانی شازە!",
  avatarUrl: shazaLogo,
  coverUrl: shazaCover,
  verified: true,
  views: 0
};

export const defaultChannels: Channel[] = [
  {
    id: 'ch-1',
    name: 'SHAZA VIP - CHANEL',
    handle: '@shazavip_chanel',
    platform: 'telegram',
    url: 'https://t.me/shazavip',
    description: 'چەناڵی فەرمی',
    clicks: 0,
    category: 'gaming',
    accentColor: '#3B82F6'
  },
  {
    id: 'ch-2',
    name: 'SHAZA VIP - KEY',
    handle: '@shazavip_key',
    platform: 'telegram',
    url: 'https://t.me/shazavip1',
    description: 'چەناڵی کلیل',
    clicks: 0,
    category: 'key',
    accentColor: '#3B82F6'
  },
  {
    id: 'ch-3',
    name: 'SHAZA VIP - CHAT',
    handle: '@shazavip2',
    platform: 'telegram',
    url: 'https://t.me/shazavip2',
    description: 'گروپ چات',
    clicks: 0,
    category: 'chat',
    accentColor: '#3B82F6'
  },
  {
    id: 'ch-4',
    name: 'SHAZA VIP - TUT',
    handle: '@shazavip3',
    platform: 'telegram',
    url: 'https://t.me/shazavip3',
    description: 'چەناڵی فێرکاری',
    clicks: 0,
    category: 'tutorial',
    accentColor: '#3B82F6'
  },
  {
    id: 'ch-5',
    name: 'SHAZA VIP - 2',
    handle: '@shazavip5',
    platform: 'telegram',
    url: 'https://t.me/shazavip5',
    description: 'چەناڵی دووەمی فەرمی',
    clicks: 0,
    category: 'gaming',
    accentColor: '#3B82F6'
  },
  {
    id: 'ch-6',
    name: 'SHAZA - OFFICIAL',
    handle: '@Hamokal4ri',
    platform: 'telegram',
    url: 'https://t.me/Hamokal4ri',
    description: 'ئەکاونتی فەرمی شازە',
    clicks: 0,
    category: 'official',
    accentColor: '#3B82F6'
  }
];

id: 'ch-7',
    name: 'SHAZA - WTA',
    handle: '@dnk_hamk',
    platform: 'telegram',
    url: 'https://t.me/dnk_hamk',
    description: 'چەناڵی وتە',
    clicks: 0,
    category: 'CHANNEL',
    accentColor: '#3B82F6'
  }
];
