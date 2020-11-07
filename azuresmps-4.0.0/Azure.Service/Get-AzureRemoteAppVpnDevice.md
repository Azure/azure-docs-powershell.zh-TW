---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DF95285F-97F4-4064-8E27-EE6E93843E55
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0a14865c986bf6439df833a38f87835792a6e3c5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967072"
---
# <span data-ttu-id="5be6d-101">Get-AzureRemoteAppVpnDevice</span><span class="sxs-lookup"><span data-stu-id="5be6d-101">Get-AzureRemoteAppVpnDevice</span></span>

## <span data-ttu-id="5be6d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5be6d-102">SYNOPSIS</span></span>
<span data-ttu-id="5be6d-103">檢索 VPN 裝置的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5be6d-103">Retrieves information about a VPN device.</span></span>

## <span data-ttu-id="5be6d-104">句法</span><span class="sxs-lookup"><span data-stu-id="5be6d-104">SYNTAX</span></span>

```
Get-AzureRemoteAppVpnDevice [-VNetName] <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5be6d-105">說明</span><span class="sxs-lookup"><span data-stu-id="5be6d-105">DESCRIPTION</span></span>
<span data-ttu-id="5be6d-106">AzureRemoteAppVpnDevice Cmdlet 會 (VPN) 裝置的虛擬私人網路絡資訊來 **取得** 相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5be6d-106">The **Get-AzureRemoteAppVpnDevice** cmdlet retrieves information about a virtual private network (VPN) device.</span></span>

## <span data-ttu-id="5be6d-107">示例</span><span class="sxs-lookup"><span data-stu-id="5be6d-107">EXAMPLES</span></span>

### <span data-ttu-id="5be6d-108">範例1：返回虛擬網路可用的 VPN 裝置設定</span><span class="sxs-lookup"><span data-stu-id="5be6d-108">Example 1: Return the available VPN device configurations for a virtual network</span></span>
```
PS C:\> Get-AzureRemoteVpnDevice -VNetName "ContosoVNet"


Name                   Platforms

----                   ---------

Cisco Systems, Inc.    {ASA 5500 Series Adaptive Security Appliances, ASR 1000 Series Aggregation Services Routers, ASR 1000 Series Aggregation Services Routers - Dynamic Routing, ISR Series Integrated Services Routers...} 

Juniper Networks, Inc. {SRX Series Routers, SRX Series Routers - Dynamic Routing, J Series Routers, J Series Routers - Dynamic Routing...} 

Microsoft Corporation  {RRAS}
```

<span data-ttu-id="5be6d-109">這個命令會傳回指定虛擬網路的可用 VPN 裝置設定。</span><span class="sxs-lookup"><span data-stu-id="5be6d-109">This command returns the available VPN device configurations for the specified virtual network.</span></span>

## <span data-ttu-id="5be6d-110">參數</span><span class="sxs-lookup"><span data-stu-id="5be6d-110">PARAMETERS</span></span>

### <span data-ttu-id="5be6d-111">-設定檔</span><span class="sxs-lookup"><span data-stu-id="5be6d-111">-Profile</span></span>
<span data-ttu-id="5be6d-112">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="5be6d-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5be6d-113">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="5be6d-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5be6d-114">-VNetName</span><span class="sxs-lookup"><span data-stu-id="5be6d-114">-VNetName</span></span>
<span data-ttu-id="5be6d-115">指定 Azure RemoteApp 虛擬網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="5be6d-115">Specifies the name of the Azure RemoteApp virtual network.</span></span>

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

### <span data-ttu-id="5be6d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5be6d-116">CommonParameters</span></span>
<span data-ttu-id="5be6d-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5be6d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5be6d-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5be6d-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5be6d-119">輸入</span><span class="sxs-lookup"><span data-stu-id="5be6d-119">INPUTS</span></span>

## <span data-ttu-id="5be6d-120">輸出</span><span class="sxs-lookup"><span data-stu-id="5be6d-120">OUTPUTS</span></span>

### <span data-ttu-id="5be6d-121">System.object</span><span class="sxs-lookup"><span data-stu-id="5be6d-121">System.String</span></span>

## <span data-ttu-id="5be6d-122">筆記</span><span class="sxs-lookup"><span data-stu-id="5be6d-122">NOTES</span></span>

## <span data-ttu-id="5be6d-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="5be6d-123">RELATED LINKS</span></span>

[<span data-ttu-id="5be6d-124">AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="5be6d-124">Get-AzureRemoteAppVNet</span></span>](./Get-AzureRemoteAppVNet.md)

[<span data-ttu-id="5be6d-125">AzureRemoteAppVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="5be6d-125">Get-AzureRemoteAppVpnDeviceConfigScript</span></span>](./Get-AzureRemoteAppVpnDeviceConfigScript.md)


