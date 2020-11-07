---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 3249E908-B1D9-4707-844D-168274F1A466
online version: ''
schema: 2.0.0
ms.openlocfilehash: ae16609adf70b2e5a0edcd05c36b30860a3920cf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967271"
---
# <span data-ttu-id="da77f-101">Set-AzureReservedIPAssociation</span><span class="sxs-lookup"><span data-stu-id="da77f-101">Set-AzureReservedIPAssociation</span></span>

## <span data-ttu-id="da77f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="da77f-102">SYNOPSIS</span></span>
<span data-ttu-id="da77f-103">將保留 IP 位址與現有的虛擬機器或雲端服務相關聯。</span><span class="sxs-lookup"><span data-stu-id="da77f-103">Associates a reserved IP address with an existing virtual machine or cloud service.</span></span>

## <span data-ttu-id="da77f-104">句法</span><span class="sxs-lookup"><span data-stu-id="da77f-104">SYNTAX</span></span>

```
Set-AzureReservedIPAssociation [-ReservedIPName] <String> [-ServiceName] <String> [[-VirtualIPName] <String>]
 [[-Slot] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="da77f-105">說明</span><span class="sxs-lookup"><span data-stu-id="da77f-105">DESCRIPTION</span></span>
<span data-ttu-id="da77f-106">**AzureReservedIPAssociation** Cmdlet 會將保留 IP 位址與正在執行的虛擬機器或雲端服務的虛擬 IP 位址 (VIP) 進行關聯。</span><span class="sxs-lookup"><span data-stu-id="da77f-106">The **Set-AzureReservedIPAssociation** cmdlet associates a reserved IP address with the Virtual IP address (VIP) of a running virtual machine or cloud service.</span></span>
<span data-ttu-id="da77f-107">在調用這個 Cmdlet 時，保留的 IP 位址一定不能使用，而且必須與虛擬機器或雲端服務位於同一個區域中。</span><span class="sxs-lookup"><span data-stu-id="da77f-107">The reserved IP address must not be in use at the time of invocation of this cmdlet, and must be in the same region as the virtual machine or cloud service.</span></span>

<span data-ttu-id="da77f-108">完成此作業大約需要30秒，之後就可以使用保留的 IP 位址來存取虛擬機器或服務。</span><span class="sxs-lookup"><span data-stu-id="da77f-108">The operation takes about 30 seconds to complete, after which the virtual machine or service is accessible using the reserved IP address.</span></span>

## <span data-ttu-id="da77f-109">示例</span><span class="sxs-lookup"><span data-stu-id="da77f-109">EXAMPLES</span></span>

### <span data-ttu-id="da77f-110">範例1：設定保留 IP 關聯</span><span class="sxs-lookup"><span data-stu-id="da77f-110">Example 1: Set a reserved IP association</span></span>
```
PS C:\> Set-AzureReservedIPAssociation -ReservedIPName "ResIp14" -ServiceName "PipTestWestEurope"
```

<span data-ttu-id="da77f-111">這個命令會將名為 ResIp14 的保留 IP 位址指派給服務 PipTestWestEurope。</span><span class="sxs-lookup"><span data-stu-id="da77f-111">This command assigns the reserved IP address named ResIp14 to the service PipTestWestEurope.</span></span>
<span data-ttu-id="da77f-112">ResIp14 是在西歐地區保留的 IP。</span><span class="sxs-lookup"><span data-stu-id="da77f-112">ResIp14 is a reserved IP in the West Europe region.</span></span>

## <span data-ttu-id="da77f-113">參數</span><span class="sxs-lookup"><span data-stu-id="da77f-113">PARAMETERS</span></span>

### <span data-ttu-id="da77f-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="da77f-114">-InformationAction</span></span>
<span data-ttu-id="da77f-115">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="da77f-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="da77f-116">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="da77f-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="da77f-117">持續</span><span class="sxs-lookup"><span data-stu-id="da77f-117">Continue</span></span>
- <span data-ttu-id="da77f-118">理會</span><span class="sxs-lookup"><span data-stu-id="da77f-118">Ignore</span></span>
- <span data-ttu-id="da77f-119">看</span><span class="sxs-lookup"><span data-stu-id="da77f-119">Inquire</span></span>
- <span data-ttu-id="da77f-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="da77f-120">SilentlyContinue</span></span>
- <span data-ttu-id="da77f-121">停止</span><span class="sxs-lookup"><span data-stu-id="da77f-121">Stop</span></span>
- <span data-ttu-id="da77f-122">封存</span><span class="sxs-lookup"><span data-stu-id="da77f-122">Suspend</span></span>

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

### <span data-ttu-id="da77f-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="da77f-123">-InformationVariable</span></span>
<span data-ttu-id="da77f-124">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="da77f-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="da77f-125">-設定檔</span><span class="sxs-lookup"><span data-stu-id="da77f-125">-Profile</span></span>
<span data-ttu-id="da77f-126">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="da77f-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="da77f-127">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="da77f-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="da77f-128">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="da77f-128">-ReservedIPName</span></span>
<span data-ttu-id="da77f-129">指定要與虛擬機器或服務建立關聯的保留 IP 位址的名稱。</span><span class="sxs-lookup"><span data-stu-id="da77f-129">Specifies the name of the reserved IP address to associate with a virtual machine or service.</span></span>

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

### <span data-ttu-id="da77f-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="da77f-130">-ServiceName</span></span>
<span data-ttu-id="da77f-131">指定部署用來關聯保留 IP 位址之部署的服務名稱。</span><span class="sxs-lookup"><span data-stu-id="da77f-131">Specifies the name of the service that has the deployment with which to associate the reserved IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da77f-132">-槽</span><span class="sxs-lookup"><span data-stu-id="da77f-132">-Slot</span></span>
<span data-ttu-id="da77f-133">指定部署槽。</span><span class="sxs-lookup"><span data-stu-id="da77f-133">Specifies the deployment slot.</span></span>
<span data-ttu-id="da77f-134">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="da77f-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="da77f-135">播放</span><span class="sxs-lookup"><span data-stu-id="da77f-135">Staging</span></span>
- <span data-ttu-id="da77f-136">出具</span><span class="sxs-lookup"><span data-stu-id="da77f-136">Production</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da77f-137">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="da77f-137">-VirtualIPName</span></span>
<span data-ttu-id="da77f-138">指定現有 VIP 的名稱，以與保留的 IP 建立關聯。</span><span class="sxs-lookup"><span data-stu-id="da77f-138">Specifies the name of an existing VIP to associate with a reserved IP.</span></span>
<span data-ttu-id="da77f-139">請參閱 Add-AzureVirtualIP 將 Vip 新增到您的雲端服務。</span><span class="sxs-lookup"><span data-stu-id="da77f-139">See Add-AzureVirtualIP to add VIPs to your cloud service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da77f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da77f-140">CommonParameters</span></span>
<span data-ttu-id="da77f-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="da77f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da77f-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="da77f-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da77f-143">輸入</span><span class="sxs-lookup"><span data-stu-id="da77f-143">INPUTS</span></span>

## <span data-ttu-id="da77f-144">輸出</span><span class="sxs-lookup"><span data-stu-id="da77f-144">OUTPUTS</span></span>

### <span data-ttu-id="da77f-145">WindowsAzure. 常見. ManagementOperationCoNtext</span><span class="sxs-lookup"><span data-stu-id="da77f-145">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="da77f-146">筆記</span><span class="sxs-lookup"><span data-stu-id="da77f-146">NOTES</span></span>

## <span data-ttu-id="da77f-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="da77f-147">RELATED LINKS</span></span>

[<span data-ttu-id="da77f-148">移除-AzureReservedIPAssociation</span><span class="sxs-lookup"><span data-stu-id="da77f-148">Remove-AzureReservedIPAssociation</span></span>](./Remove-AzureReservedIPAssociation.md)


