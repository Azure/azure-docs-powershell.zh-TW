---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 4522E93F-6AC9-4A37-88B8-CCCCE15A5879
online version: ''
schema: 2.0.0
ms.openlocfilehash: fcfc41e06f6847612c275817560e8593b76f6bac
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966917"
---
# <span data-ttu-id="aa012-101">Reset-AzureRemoteAppVpnSharedKey</span><span class="sxs-lookup"><span data-stu-id="aa012-101">Reset-AzureRemoteAppVpnSharedKey</span></span>

## <span data-ttu-id="aa012-102">摘要</span><span class="sxs-lookup"><span data-stu-id="aa012-102">SYNOPSIS</span></span>
<span data-ttu-id="aa012-103">重設 Azure RemoteApp VPN 共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="aa012-103">Resets the Azure RemoteApp VPN shared key.</span></span>

## <span data-ttu-id="aa012-104">句法</span><span class="sxs-lookup"><span data-stu-id="aa012-104">SYNTAX</span></span>

```
Reset-AzureRemoteAppVpnSharedKey [-VNetName] <String> [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aa012-105">說明</span><span class="sxs-lookup"><span data-stu-id="aa012-105">DESCRIPTION</span></span>
<span data-ttu-id="aa012-106">**Reset AzureRemoteAppVpnSharedKey** Cmdlet 會將 Azure RemoteApp 虛擬私人網路絡 (VPN 重設) 共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="aa012-106">The **Reset-AzureRemoteAppVpnSharedKey** cmdlet resets the Azure RemoteApp virtual private network (VPN) shared key.</span></span>

## <span data-ttu-id="aa012-107">示例</span><span class="sxs-lookup"><span data-stu-id="aa012-107">EXAMPLES</span></span>

### <span data-ttu-id="aa012-108">範例1：重設虛擬網路上的共用金鑰</span><span class="sxs-lookup"><span data-stu-id="aa012-108">Example 1: Reset the shared key on a virtual network</span></span>
```
PS C:\> Reset-AzureRemoteAppVpnSharedKey -VNetName "ContosoVNet"
```

<span data-ttu-id="aa012-109">這個命令會在名為 ContosoVNet 的虛擬網路上重設共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="aa012-109">This command resets the shared key on the virtual network named ContosoVNet.</span></span>
<span data-ttu-id="aa012-110">在 VPN 裝置上設定新的共用金鑰之前，到內部部署網路的 VPN 連線會保持離線。</span><span class="sxs-lookup"><span data-stu-id="aa012-110">The VPN connection to the on-premises network remains offline until the new shared key is configured on the VPN device.</span></span>
<span data-ttu-id="aa012-111">若要設定 VPN 裝置，請使用 **AzureRemoteAppVpnDeviceConfigScript** Cmdlet 來為您的 vpn 裝置取得正確的腳本或配置檔案，然後將該腳本或設定檔載入到 vpn 裝置。</span><span class="sxs-lookup"><span data-stu-id="aa012-111">To configure the VPN device, use the **Get-AzureRemoteAppVpnDeviceConfigScript** cmdlet to retrieve the correct script or configuration file for your VPN device, then load that script or configuration file onto the VPN device.</span></span>

## <span data-ttu-id="aa012-112">參數</span><span class="sxs-lookup"><span data-stu-id="aa012-112">PARAMETERS</span></span>

### <span data-ttu-id="aa012-113">-設定檔</span><span class="sxs-lookup"><span data-stu-id="aa012-113">-Profile</span></span>
<span data-ttu-id="aa012-114">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="aa012-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="aa012-115">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="aa012-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa012-116">-VNetName</span><span class="sxs-lookup"><span data-stu-id="aa012-116">-VNetName</span></span>
<span data-ttu-id="aa012-117">指定 Azure RemoteApp 虛擬網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="aa012-117">Specifies the name of the Azure RemoteApp virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aa012-118">-確認</span><span class="sxs-lookup"><span data-stu-id="aa012-118">-Confirm</span></span>
<span data-ttu-id="aa012-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="aa012-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa012-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa012-120">-WhatIf</span></span>
<span data-ttu-id="aa012-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="aa012-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa012-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="aa012-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa012-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa012-123">CommonParameters</span></span>
<span data-ttu-id="aa012-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="aa012-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa012-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="aa012-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa012-126">輸入</span><span class="sxs-lookup"><span data-stu-id="aa012-126">INPUTS</span></span>

## <span data-ttu-id="aa012-127">輸出</span><span class="sxs-lookup"><span data-stu-id="aa012-127">OUTPUTS</span></span>

### <span data-ttu-id="aa012-128">System.object</span><span class="sxs-lookup"><span data-stu-id="aa012-128">System.String</span></span>

## <span data-ttu-id="aa012-129">筆記</span><span class="sxs-lookup"><span data-stu-id="aa012-129">NOTES</span></span>

## <span data-ttu-id="aa012-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="aa012-130">RELATED LINKS</span></span>

[<span data-ttu-id="aa012-131">AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="aa012-131">Get-AzureRemoteAppVNet</span></span>](./Get-AzureRemoteAppVNet.md)

[<span data-ttu-id="aa012-132">AzureRemoteAppVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="aa012-132">Get-AzureRemoteAppVpnDeviceConfigScript</span></span>](./Get-AzureRemoteAppVpnDeviceConfigScript.md)


