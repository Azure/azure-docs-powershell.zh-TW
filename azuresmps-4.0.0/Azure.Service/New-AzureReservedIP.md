---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9C22F5D7-1FD0-4699-83D7-1D72C5234DEF
online version: ''
schema: 2.0.0
ms.openlocfilehash: d09173c43de9c01056055f714217db5eb4c58225
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967439"
---
# <span data-ttu-id="cc269-101">New-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="cc269-101">New-AzureReservedIP</span></span>

## <span data-ttu-id="cc269-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cc269-102">SYNOPSIS</span></span>
<span data-ttu-id="cc269-103">建立保留的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="cc269-103">Creates a reserved IP address.</span></span>

## <span data-ttu-id="cc269-104">句法</span><span class="sxs-lookup"><span data-stu-id="cc269-104">SYNTAX</span></span>

### <span data-ttu-id="cc269-105">CreateNewReservedIP (預設) </span><span class="sxs-lookup"><span data-stu-id="cc269-105">CreateNewReservedIP (Default)</span></span>
```
New-AzureReservedIP [-ReservedIPName] <String> [[-Label] <String>] [-Location] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="cc269-106">CreateInUseReservedIPUsingSlot</span><span class="sxs-lookup"><span data-stu-id="cc269-106">CreateInUseReservedIPUsingSlot</span></span>
```
New-AzureReservedIP [-ReservedIPName] <String> [[-Label] <String>] [-Location] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="cc269-107">CreateInUseReservedIP</span><span class="sxs-lookup"><span data-stu-id="cc269-107">CreateInUseReservedIP</span></span>
```
New-AzureReservedIP [-ReservedIPName] <String> [[-Label] <String>] [-Location] <String> [-ServiceName] <String>
 [[-VirtualIPName] <String>] [[-Slot] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="cc269-108">說明</span><span class="sxs-lookup"><span data-stu-id="cc269-108">DESCRIPTION</span></span>
<span data-ttu-id="cc269-109">**新的-AzureReservedIP** Cmdlet 會建立保留的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="cc269-109">The **New-AzureReservedIP** cmdlet creates a reserved IP address.</span></span>

## <span data-ttu-id="cc269-110">示例</span><span class="sxs-lookup"><span data-stu-id="cc269-110">EXAMPLES</span></span>

### <span data-ttu-id="cc269-111">範例1：建立新的保留 IP</span><span class="sxs-lookup"><span data-stu-id="cc269-111">Example 1: Create a new reserved IP</span></span>
```
PS C:\> New-AzureReservedIP -ReservedIPName $Name -Label $Label -Location $Location
```

<span data-ttu-id="cc269-112">這個命令會在訂閱中建立新的保留 IP 位址，這可以用來建立包含 Web、Worker 和虛擬機器的雲端服務。</span><span class="sxs-lookup"><span data-stu-id="cc269-112">This command creates a new reserved IP address in the subscription, which can be used for creating cloud services that include Web, Worker, and Virtual Machines.</span></span>

### <span data-ttu-id="cc269-113">範例2：根據現有 IP 建立保留 IP</span><span class="sxs-lookup"><span data-stu-id="cc269-113">Example 2: Create a reserved IP based on an existing IP</span></span>
```
PS C:\> New-AzureReservedIP -ReservedIPName resip14 -Location "West Europe" -ServiceName piptestwesteurope
```

<span data-ttu-id="cc269-114">這個命令會在指定的服務上建立現有的 VIP (虛擬 IP) 。</span><span class="sxs-lookup"><span data-stu-id="cc269-114">This command creates an existing VIP (Virtual IP) on the specified service.</span></span>

## <span data-ttu-id="cc269-115">參數</span><span class="sxs-lookup"><span data-stu-id="cc269-115">PARAMETERS</span></span>

### <span data-ttu-id="cc269-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="cc269-116">-InformationAction</span></span>
<span data-ttu-id="cc269-117">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="cc269-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="cc269-118">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="cc269-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cc269-119">持續</span><span class="sxs-lookup"><span data-stu-id="cc269-119">Continue</span></span>
- <span data-ttu-id="cc269-120">理會</span><span class="sxs-lookup"><span data-stu-id="cc269-120">Ignore</span></span>
- <span data-ttu-id="cc269-121">看</span><span class="sxs-lookup"><span data-stu-id="cc269-121">Inquire</span></span>
- <span data-ttu-id="cc269-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="cc269-122">SilentlyContinue</span></span>
- <span data-ttu-id="cc269-123">停止</span><span class="sxs-lookup"><span data-stu-id="cc269-123">Stop</span></span>
- <span data-ttu-id="cc269-124">封存</span><span class="sxs-lookup"><span data-stu-id="cc269-124">Suspend</span></span>

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

### <span data-ttu-id="cc269-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="cc269-125">-InformationVariable</span></span>
<span data-ttu-id="cc269-126">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="cc269-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="cc269-127">-標籤</span><span class="sxs-lookup"><span data-stu-id="cc269-127">-Label</span></span>
<span data-ttu-id="cc269-128">指定保留 IP 位址的標籤。</span><span class="sxs-lookup"><span data-stu-id="cc269-128">Specifies a label for the reserved IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc269-129">-位置</span><span class="sxs-lookup"><span data-stu-id="cc269-129">-Location</span></span>
<span data-ttu-id="cc269-130">指定要建立保留 IP 位址的位置。</span><span class="sxs-lookup"><span data-stu-id="cc269-130">Specifies a location at which to create the reserved IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc269-131">-設定檔</span><span class="sxs-lookup"><span data-stu-id="cc269-131">-Profile</span></span>
<span data-ttu-id="cc269-132">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="cc269-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cc269-133">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="cc269-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cc269-134">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="cc269-134">-ReservedIPName</span></span>
<span data-ttu-id="cc269-135">指定保留的 IP 位址名稱。</span><span class="sxs-lookup"><span data-stu-id="cc269-135">Specifies the reserved IP address name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc269-136">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="cc269-136">-ServiceName</span></span>
<span data-ttu-id="cc269-137">指定服務名稱。</span><span class="sxs-lookup"><span data-stu-id="cc269-137">Specifies a service name.</span></span>

```yaml
Type: String
Parameter Sets: CreateInUseReservedIP
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc269-138">-槽</span><span class="sxs-lookup"><span data-stu-id="cc269-138">-Slot</span></span>
<span data-ttu-id="cc269-139">指定部署槽。</span><span class="sxs-lookup"><span data-stu-id="cc269-139">Specifies the deployment slot.</span></span>
<span data-ttu-id="cc269-140">此參數可接受的值為：暫存、生產。</span><span class="sxs-lookup"><span data-stu-id="cc269-140">The acceptable values for this parameter are: Staging, Production.</span></span>

```yaml
Type: String
Parameter Sets: CreateInUseReservedIP
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc269-141">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="cc269-141">-VirtualIPName</span></span>
<span data-ttu-id="cc269-142">指定這個 Cmdlet 在您的部署中使用 **VirtualIPName** 參數來保留現有的虛擬 IP 位址 (VIP) 。</span><span class="sxs-lookup"><span data-stu-id="cc269-142">Specifies that this cmdlet uses the **VirtualIPName** parameter to reserve an existing virtual IP address (VIP) in your deployment.</span></span>
<span data-ttu-id="cc269-143">如果未指定此參數，此 Cmdlet 會保留新的 VIP。</span><span class="sxs-lookup"><span data-stu-id="cc269-143">If this parameter is not specified, this cmdlet reserves a new VIP.</span></span>

```yaml
Type: String
Parameter Sets: CreateInUseReservedIP
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc269-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc269-144">CommonParameters</span></span>
<span data-ttu-id="cc269-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cc269-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc269-146">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cc269-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc269-147">輸入</span><span class="sxs-lookup"><span data-stu-id="cc269-147">INPUTS</span></span>

## <span data-ttu-id="cc269-148">輸出</span><span class="sxs-lookup"><span data-stu-id="cc269-148">OUTPUTS</span></span>

## <span data-ttu-id="cc269-149">筆記</span><span class="sxs-lookup"><span data-stu-id="cc269-149">NOTES</span></span>

## <span data-ttu-id="cc269-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="cc269-150">RELATED LINKS</span></span>

[<span data-ttu-id="cc269-151">AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="cc269-151">Get-AzureReservedIP</span></span>](./Get-AzureReservedIP.md)

[<span data-ttu-id="cc269-152">移除-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="cc269-152">Remove-AzureReservedIP</span></span>](./Remove-AzureReservedIP.md)


