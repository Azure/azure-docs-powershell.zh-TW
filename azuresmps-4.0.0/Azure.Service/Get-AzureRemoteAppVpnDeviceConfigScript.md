---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: D0E8B2BD-D68F-477A-9D66-C27AB737960D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 59423aa3de5ae91abe82090054fac61f3901363c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967071"
---
# <span data-ttu-id="e4527-101">Get-AzureRemoteAppVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="e4527-101">Get-AzureRemoteAppVpnDeviceConfigScript</span></span>

## <span data-ttu-id="e4527-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e4527-102">SYNOPSIS</span></span>
<span data-ttu-id="e4527-103">檢索 Azure RemoteApp VPN 裝置的配置腳本。</span><span class="sxs-lookup"><span data-stu-id="e4527-103">Retrieves the configuration script for an Azure RemoteApp VPN device.</span></span>

## <span data-ttu-id="e4527-104">句法</span><span class="sxs-lookup"><span data-stu-id="e4527-104">SYNTAX</span></span>

```
Get-AzureRemoteAppVpnDeviceConfigScript [-VNetName] <String> [-Vendor] <String> [-Platform] <String>
 [-OSFamily] <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e4527-105">說明</span><span class="sxs-lookup"><span data-stu-id="e4527-105">DESCRIPTION</span></span>
<span data-ttu-id="e4527-106">AzureRemoteAppVpnDeviceConfigScript Cmdlet 會將 Azure RemoteApp 虛擬私人網路絡的設定腳本（ (VPN) 裝置） **取得** 。</span><span class="sxs-lookup"><span data-stu-id="e4527-106">The **Get-AzureRemoteAppVpnDeviceConfigScript** cmdlet retrieves the configuration script for an Azure RemoteApp virtual private network (VPN) device.</span></span>

## <span data-ttu-id="e4527-107">示例</span><span class="sxs-lookup"><span data-stu-id="e4527-107">EXAMPLES</span></span>

### <span data-ttu-id="e4527-108">範例1：取得 VPN 裝置的配置腳本</span><span class="sxs-lookup"><span data-stu-id="e4527-108">Example 1: Get a configuration script for a VPN device</span></span>
```
PS C:\> Get-AzureRemoteAppVpnDeviceConfigScript -VNetName "ContosoVNet" -Vendor "Microsoft Corporation" -OSFamily "Windows Server 2012 R2"
```

<span data-ttu-id="e4527-109">這個命令會傳回用來為名為 ContosoVNet 的虛擬網路設定 VPN 裝置的腳本或設定檔。</span><span class="sxs-lookup"><span data-stu-id="e4527-109">This command returns the script or configuration file used to configure the VPN device for the virtual network named ContosoVNet.</span></span>
<span data-ttu-id="e4527-110">此腳本或設定檔應該在 VPN 裝置上執行或載入至該裝置的一般方式。</span><span class="sxs-lookup"><span data-stu-id="e4527-110">This script or configuration file should be run or loaded onto the VPN device in the typical manner for that device.</span></span>
<span data-ttu-id="e4527-111">針對每個裝置的獨特需求，請諮詢 VPN 裝置轉銷商。</span><span class="sxs-lookup"><span data-stu-id="e4527-111">Consult the VPN device vendor for the unique requirements for each device.</span></span>

## <span data-ttu-id="e4527-112">參數</span><span class="sxs-lookup"><span data-stu-id="e4527-112">PARAMETERS</span></span>

### <span data-ttu-id="e4527-113">-OSFamily</span><span class="sxs-lookup"><span data-stu-id="e4527-113">-OSFamily</span></span>
<span data-ttu-id="e4527-114">指定在裝置平臺上執行 (OS) 系列的作業系統。</span><span class="sxs-lookup"><span data-stu-id="e4527-114">Specifies the operating system (OS) family that runs on the device platform.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4527-115">-平臺</span><span class="sxs-lookup"><span data-stu-id="e4527-115">-Platform</span></span>
<span data-ttu-id="e4527-116">指定裝置平臺。</span><span class="sxs-lookup"><span data-stu-id="e4527-116">Specifies the device platform.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4527-117">-設定檔</span><span class="sxs-lookup"><span data-stu-id="e4527-117">-Profile</span></span>
<span data-ttu-id="e4527-118">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="e4527-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e4527-119">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="e4527-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e4527-120">-供應商</span><span class="sxs-lookup"><span data-stu-id="e4527-120">-Vendor</span></span>
<span data-ttu-id="e4527-121">指定 VPN 裝置的供應商。</span><span class="sxs-lookup"><span data-stu-id="e4527-121">Specifies the vendor of the VPN device.</span></span>

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

### <span data-ttu-id="e4527-122">-VNetName</span><span class="sxs-lookup"><span data-stu-id="e4527-122">-VNetName</span></span>
<span data-ttu-id="e4527-123">指定 Azure RemoteApp 虛擬網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="e4527-123">Specifies the name of an Azure RemoteApp virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4527-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4527-124">CommonParameters</span></span>
<span data-ttu-id="e4527-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e4527-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4527-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e4527-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4527-127">輸入</span><span class="sxs-lookup"><span data-stu-id="e4527-127">INPUTS</span></span>

## <span data-ttu-id="e4527-128">輸出</span><span class="sxs-lookup"><span data-stu-id="e4527-128">OUTPUTS</span></span>

## <span data-ttu-id="e4527-129">筆記</span><span class="sxs-lookup"><span data-stu-id="e4527-129">NOTES</span></span>

## <span data-ttu-id="e4527-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="e4527-130">RELATED LINKS</span></span>

[<span data-ttu-id="e4527-131">AzureRemoteAppVpnDevice</span><span class="sxs-lookup"><span data-stu-id="e4527-131">Get-AzureRemoteAppVpnDevice</span></span>](./Get-AzureRemoteAppVpnDevice.md)


