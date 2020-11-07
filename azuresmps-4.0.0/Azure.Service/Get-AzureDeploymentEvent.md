---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6715B3E8-6880-4B86-B831-41664766E12B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 026e06a0071084f07ed0b609b8b686e6cba44cc5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967096"
---
# <span data-ttu-id="3f7ce-101">Get-AzureDeploymentEvent</span><span class="sxs-lookup"><span data-stu-id="3f7ce-101">Get-AzureDeploymentEvent</span></span>

## <span data-ttu-id="3f7ce-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3f7ce-102">SYNOPSIS</span></span>
<span data-ttu-id="3f7ce-103">取得 Azure 啟動並影響虛擬機器和雲端服務之事件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3f7ce-103">Gets information about events that Azure initiates that impact virtual machines and cloud services.</span></span>

## <span data-ttu-id="3f7ce-104">句法</span><span class="sxs-lookup"><span data-stu-id="3f7ce-104">SYNTAX</span></span>

### <span data-ttu-id="3f7ce-105">GetDeploymentEventBySlot (預設) </span><span class="sxs-lookup"><span data-stu-id="3f7ce-105">GetDeploymentEventBySlot (Default)</span></span>
```
Get-AzureDeploymentEvent [-ServiceName] <String> [-StartTime] <DateTime> [-EndTime] <DateTime>
 [[-Slot] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="3f7ce-106">GetDeploymentEventByName</span><span class="sxs-lookup"><span data-stu-id="3f7ce-106">GetDeploymentEventByName</span></span>
```
Get-AzureDeploymentEvent [-ServiceName] <String> [-StartTime] <DateTime> [-EndTime] <DateTime>
 [-DeploymentName] <String> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="3f7ce-107">說明</span><span class="sxs-lookup"><span data-stu-id="3f7ce-107">DESCRIPTION</span></span>
<span data-ttu-id="3f7ce-108">**AzureDeploymentEvent** Cmdlet 會取得 Azure 啟動並影響虛擬機器和雲端服務之事件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3f7ce-108">The **Get-AzureDeploymentEvent** cmdlet gets information regarding events that Azure initiates that impact virtual machines and cloud services.</span></span>
<span data-ttu-id="3f7ce-109">這些事件包含規劃的維護活動。</span><span class="sxs-lookup"><span data-stu-id="3f7ce-109">These events include planned maintenance events.</span></span>
<span data-ttu-id="3f7ce-110">這個 Cmdlet 會傳回事件的清單，這些事件可識別受影響的角色實例或虛擬機器、影響的原因，以及事件的開始時間。</span><span class="sxs-lookup"><span data-stu-id="3f7ce-110">This cmdlet returns a list of events that identify the role instance or virtual machine impacted, the reason for the impact, and the start time of the event.</span></span>

## <span data-ttu-id="3f7ce-111">示例</span><span class="sxs-lookup"><span data-stu-id="3f7ce-111">EXAMPLES</span></span>

### <span data-ttu-id="3f7ce-112">sr-1</span><span class="sxs-lookup"><span data-stu-id="3f7ce-112">1:</span></span>
```
Get-AzureDeploymentEvent -DeploymentName "ConstosoDeployment" -ServiceName "ContosoService"
```

## <span data-ttu-id="3f7ce-113">參數</span><span class="sxs-lookup"><span data-stu-id="3f7ce-113">PARAMETERS</span></span>

### <span data-ttu-id="3f7ce-114">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="3f7ce-114">-DeploymentName</span></span>
<span data-ttu-id="3f7ce-115">指定此 Cmdlet 取得事件之部署的名稱。</span><span class="sxs-lookup"><span data-stu-id="3f7ce-115">Specifies the name of the deployment for which this cmdlet gets events.</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentEventByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f7ce-116">-EndTime</span><span class="sxs-lookup"><span data-stu-id="3f7ce-116">-EndTime</span></span>
<span data-ttu-id="3f7ce-117">指定此 Cmdlet 取得的排程事件的結束時間。</span><span class="sxs-lookup"><span data-stu-id="3f7ce-117">Specifies the ending time for the scheduled events that this cmdlet gets.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f7ce-118">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="3f7ce-118">-InformationAction</span></span>
<span data-ttu-id="3f7ce-119">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="3f7ce-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3f7ce-120">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="3f7ce-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3f7ce-121">持續</span><span class="sxs-lookup"><span data-stu-id="3f7ce-121">Continue</span></span>
- <span data-ttu-id="3f7ce-122">理會</span><span class="sxs-lookup"><span data-stu-id="3f7ce-122">Ignore</span></span>
- <span data-ttu-id="3f7ce-123">看</span><span class="sxs-lookup"><span data-stu-id="3f7ce-123">Inquire</span></span>
- <span data-ttu-id="3f7ce-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3f7ce-124">SilentlyContinue</span></span>
- <span data-ttu-id="3f7ce-125">停止</span><span class="sxs-lookup"><span data-stu-id="3f7ce-125">Stop</span></span>
- <span data-ttu-id="3f7ce-126">封存</span><span class="sxs-lookup"><span data-stu-id="3f7ce-126">Suspend</span></span>

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

### <span data-ttu-id="3f7ce-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3f7ce-127">-InformationVariable</span></span>
<span data-ttu-id="3f7ce-128">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="3f7ce-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="3f7ce-129">-設定檔</span><span class="sxs-lookup"><span data-stu-id="3f7ce-129">-Profile</span></span>
<span data-ttu-id="3f7ce-130">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="3f7ce-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3f7ce-131">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="3f7ce-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3f7ce-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="3f7ce-132">-ServiceName</span></span>
<span data-ttu-id="3f7ce-133">指定此 Cmdlet 用來取得排程事件之託管服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="3f7ce-133">Specifies the name of the hosted service for which this cmdlet gets scheduled events.</span></span>

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

### <span data-ttu-id="3f7ce-134">-槽</span><span class="sxs-lookup"><span data-stu-id="3f7ce-134">-Slot</span></span>
<span data-ttu-id="3f7ce-135">指定此 Cmdlet 取得排程事件的部署環境。</span><span class="sxs-lookup"><span data-stu-id="3f7ce-135">Specifies the environment of the deployment for which this cmdlet gets scheduled events.</span></span>
<span data-ttu-id="3f7ce-136">有效值為：暫存與生產。</span><span class="sxs-lookup"><span data-stu-id="3f7ce-136">Valid values are: Staging and Production.</span></span>
<span data-ttu-id="3f7ce-137">預設值為 [生產]。</span><span class="sxs-lookup"><span data-stu-id="3f7ce-137">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentEventBySlot
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f7ce-138">-StartTime</span><span class="sxs-lookup"><span data-stu-id="3f7ce-138">-StartTime</span></span>
<span data-ttu-id="3f7ce-139">指定此 Cmdlet 取得的排程事件的開始時間。</span><span class="sxs-lookup"><span data-stu-id="3f7ce-139">Specifies the starting time for the scheduled events that this cmdlet gets.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f7ce-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f7ce-140">CommonParameters</span></span>
<span data-ttu-id="3f7ce-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3f7ce-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f7ce-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3f7ce-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f7ce-143">輸入</span><span class="sxs-lookup"><span data-stu-id="3f7ce-143">INPUTS</span></span>

## <span data-ttu-id="3f7ce-144">輸出</span><span class="sxs-lookup"><span data-stu-id="3f7ce-144">OUTPUTS</span></span>

## <span data-ttu-id="3f7ce-145">筆記</span><span class="sxs-lookup"><span data-stu-id="3f7ce-145">NOTES</span></span>

## <span data-ttu-id="3f7ce-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="3f7ce-146">RELATED LINKS</span></span>

[<span data-ttu-id="3f7ce-147">AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="3f7ce-147">Get-AzureDeployment</span></span>](./Get-AzureDeployment.md)


