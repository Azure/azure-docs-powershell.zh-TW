---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 895F9A5F-D48F-403D-BD8F-72D72D420690
online version: ''
schema: 2.0.0
ms.openlocfilehash: 97bb3e07f5c6df25e7c03c167cc4cb49c25f9414
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967233"
---
# <span data-ttu-id="e6821-101">Set-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="e6821-101">Set-AzureVNetConfig</span></span>

## <span data-ttu-id="e6821-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e6821-102">SYNOPSIS</span></span>
<span data-ttu-id="e6821-103">更新 Azure 雲端服務的虛擬網路設定。</span><span class="sxs-lookup"><span data-stu-id="e6821-103">Updates the virtual network settings for an Azure cloud service.</span></span>

## <span data-ttu-id="e6821-104">句法</span><span class="sxs-lookup"><span data-stu-id="e6821-104">SYNTAX</span></span>

```
Set-AzureVNetConfig [-ConfigurationPath] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="e6821-105">說明</span><span class="sxs-lookup"><span data-stu-id="e6821-105">DESCRIPTION</span></span>
<span data-ttu-id="e6821-106">**AzureVNetConfig** Cmdlet 會透過指定網路設定檔案的路徑來更新目前 Azure 訂閱的網路設定，方法是將) 的網路設定 ( 檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="e6821-106">The **Set-AzureVNetConfig** cmdlet updates the network configuration for the current Azure subscription by specifying a path to a network configuration file (.netcfg).</span></span>
<span data-ttu-id="e6821-107">網路設定檔會定義訂閱中雲端服務的 DNS 伺服器和子網。</span><span class="sxs-lookup"><span data-stu-id="e6821-107">The network configuration file defines DNS servers and subnets for cloud services within a subscription.</span></span>

## <span data-ttu-id="e6821-108">示例</span><span class="sxs-lookup"><span data-stu-id="e6821-108">EXAMPLES</span></span>

### <span data-ttu-id="e6821-109">範例1：將 Azure 訂閱的網路設定更新為本機檔案</span><span class="sxs-lookup"><span data-stu-id="e6821-109">Example 1: Update the network configuration of the Azure subscription to a local file</span></span>
```
PS C:\> Set-AzureVNetConfig  -ConfigurationPath "c:\temp\MyAzNets.netcfg"
```

<span data-ttu-id="e6821-110">這個命令會將目前 Microsoft Azure 訂閱的網路設定更新為本機檔案 "c:\temp\MyAzNets.netcfg" 中的內容。</span><span class="sxs-lookup"><span data-stu-id="e6821-110">This command updates the network configuration of the current Microsoft Azure subscription to that in the local file "c:\temp\MyAzNets.netcfg".</span></span>

### <span data-ttu-id="e6821-111">範例2：設定 Azure 訂閱，然後更新網路設定</span><span class="sxs-lookup"><span data-stu-id="e6821-111">Example 2: Set the Azure subscription and then update the network configuration</span></span>
```
PS C:\> $SubsId = "5bea2bc2-88a5-44b8-abe1-3e76733b6783"
C:\PS> $Cert = Get-Item cert:\LocalMachine\MY\82F105B2DA81149204A6257A9A91EC452B8C52C3
C:\PS> Set-AzureVNetConfig  -ConfigurationPath "c:\temp\MyAzNets.netcfg"
```

<span data-ttu-id="e6821-112">這個範例會設定 Microsoft Azure 訂閱，然後使用本機檔案 "c:\temp\MyAzNets.netcfg" 中定義的設定來更新該訂閱的網路設定。</span><span class="sxs-lookup"><span data-stu-id="e6821-112">This example sets the Microsoft Azure subscription, and then updates the network configuration of that subscription using the configuration defined in the local file "c:\temp\MyAzNets.netcfg".</span></span>

## <span data-ttu-id="e6821-113">參數</span><span class="sxs-lookup"><span data-stu-id="e6821-113">PARAMETERS</span></span>

### <span data-ttu-id="e6821-114">-ConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="e6821-114">-ConfigurationPath</span></span>
<span data-ttu-id="e6821-115">指定網路設定檔的路徑和檔案名 () 。</span><span class="sxs-lookup"><span data-stu-id="e6821-115">Specifies the path and file name of a network configuration file (.netcfg).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6821-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="e6821-116">-InformationAction</span></span>
<span data-ttu-id="e6821-117">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="e6821-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e6821-118">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="e6821-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e6821-119">持續</span><span class="sxs-lookup"><span data-stu-id="e6821-119">Continue</span></span>
- <span data-ttu-id="e6821-120">理會</span><span class="sxs-lookup"><span data-stu-id="e6821-120">Ignore</span></span>
- <span data-ttu-id="e6821-121">看</span><span class="sxs-lookup"><span data-stu-id="e6821-121">Inquire</span></span>
- <span data-ttu-id="e6821-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e6821-122">SilentlyContinue</span></span>
- <span data-ttu-id="e6821-123">停止</span><span class="sxs-lookup"><span data-stu-id="e6821-123">Stop</span></span>
- <span data-ttu-id="e6821-124">封存</span><span class="sxs-lookup"><span data-stu-id="e6821-124">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6821-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e6821-125">-InformationVariable</span></span>
<span data-ttu-id="e6821-126">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="e6821-126">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6821-127">-設定檔</span><span class="sxs-lookup"><span data-stu-id="e6821-127">-Profile</span></span>
<span data-ttu-id="e6821-128">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="e6821-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e6821-129">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="e6821-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e6821-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6821-130">CommonParameters</span></span>
<span data-ttu-id="e6821-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e6821-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6821-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e6821-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6821-133">輸入</span><span class="sxs-lookup"><span data-stu-id="e6821-133">INPUTS</span></span>

## <span data-ttu-id="e6821-134">輸出</span><span class="sxs-lookup"><span data-stu-id="e6821-134">OUTPUTS</span></span>

## <span data-ttu-id="e6821-135">筆記</span><span class="sxs-lookup"><span data-stu-id="e6821-135">NOTES</span></span>

## <span data-ttu-id="e6821-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="e6821-136">RELATED LINKS</span></span>

[<span data-ttu-id="e6821-137">AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="e6821-137">Get-AzureVNetConfig</span></span>](./Get-AzureVNetConfig.md)

[<span data-ttu-id="e6821-138">AzureVNetSite</span><span class="sxs-lookup"><span data-stu-id="e6821-138">Get-AzureVNetSite</span></span>](./Get-AzureVNetSite.md)

[<span data-ttu-id="e6821-139">移除-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="e6821-139">Remove-AzureVNetConfig</span></span>](./Remove-AzureVNetConfig.md)


