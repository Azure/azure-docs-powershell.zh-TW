---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7317DAC1-B535-4650-86BF-73E96F61EECD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 23bb8e09fac8ec4fe0e8ff5b3c23ab995f03694c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967637"
---
# <span data-ttu-id="9c790-101">New-AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="9c790-101">New-AzureVMSqlServerAutoPatchingConfig</span></span>

## <span data-ttu-id="9c790-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9c790-102">SYNOPSIS</span></span>
<span data-ttu-id="9c790-103">建立虛擬機器自動修補的設定物件。</span><span class="sxs-lookup"><span data-stu-id="9c790-103">Creates a configuration object for virtual machine automatic patching.</span></span>

## <span data-ttu-id="9c790-104">句法</span><span class="sxs-lookup"><span data-stu-id="9c790-104">SYNTAX</span></span>

```
New-AzureVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="9c790-105">說明</span><span class="sxs-lookup"><span data-stu-id="9c790-105">DESCRIPTION</span></span>
<span data-ttu-id="9c790-106">**新的-AzureVMSqlServerAutoPatchingConfig** Cmdlet 會建立虛擬機器自動修補的設定物件。</span><span class="sxs-lookup"><span data-stu-id="9c790-106">The **New-AzureVMSqlServerAutoPatchingConfig** cmdlet creates a configuration object for virtual machine automatic patching.</span></span>

## <span data-ttu-id="9c790-107">示例</span><span class="sxs-lookup"><span data-stu-id="9c790-107">EXAMPLES</span></span>

### <span data-ttu-id="9c790-108">範例1：建立設定物件以設定自動修補</span><span class="sxs-lookup"><span data-stu-id="9c790-108">Example 1: Create a configuration object to configure automatic patching</span></span>
```
PS C:\> $APS = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
          Enable                        : True
          DayOfWeek                     : Thursday
          MaintenanceWindowStartingHour : 11
          MaintenanceWindowDuration     : 120
          PatchCategory                 : Important
```

<span data-ttu-id="9c790-109">這個命令會建立可讓您使用設定 AzureVMSqlServerExtension 來設定自動修補的設定物件。</span><span class="sxs-lookup"><span data-stu-id="9c790-109">This command creates configuration object that can be used to configure automatic patching using Set-AzureVMSqlServerExtension.</span></span>

## <span data-ttu-id="9c790-110">參數</span><span class="sxs-lookup"><span data-stu-id="9c790-110">PARAMETERS</span></span>

### <span data-ttu-id="9c790-111">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="9c790-111">-DayOfWeek</span></span>
<span data-ttu-id="9c790-112">指定一周中要安裝更新的日期。</span><span class="sxs-lookup"><span data-stu-id="9c790-112">Specifies the day of the week when updates should be installed.</span></span>

<span data-ttu-id="9c790-113">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="9c790-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9c790-114">日</span><span class="sxs-lookup"><span data-stu-id="9c790-114">Sunday</span></span>
- <span data-ttu-id="9c790-115">從</span><span class="sxs-lookup"><span data-stu-id="9c790-115">Monday</span></span>
- <span data-ttu-id="9c790-116">星期二</span><span class="sxs-lookup"><span data-stu-id="9c790-116">Tuesday</span></span>
- <span data-ttu-id="9c790-117">星期三</span><span class="sxs-lookup"><span data-stu-id="9c790-117">Wednesday</span></span>
- <span data-ttu-id="9c790-118">星期四</span><span class="sxs-lookup"><span data-stu-id="9c790-118">Thursday</span></span>
- <span data-ttu-id="9c790-119">日</span><span class="sxs-lookup"><span data-stu-id="9c790-119">Friday</span></span>
- <span data-ttu-id="9c790-120">星期六</span><span class="sxs-lookup"><span data-stu-id="9c790-120">Saturday</span></span>
- <span data-ttu-id="9c790-121">生活</span><span class="sxs-lookup"><span data-stu-id="9c790-121">Everyday</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c790-122">-啟用</span><span class="sxs-lookup"><span data-stu-id="9c790-122">-Enable</span></span>
<span data-ttu-id="9c790-123">表示已啟用虛擬機器的自動修補程式。</span><span class="sxs-lookup"><span data-stu-id="9c790-123">Indicates that automated patching for the virtual machine is enabled.</span></span>
<span data-ttu-id="9c790-124">如果您啟用自動修補程式，則 Cmdlet 會將 Windows 更新到互動模式。</span><span class="sxs-lookup"><span data-stu-id="9c790-124">If you enable automated patching the cmdlet will put Windows Update into interactive mode.</span></span>
<span data-ttu-id="9c790-125">如果您停用自動修補程式，Windows 更新設定將不會變更。</span><span class="sxs-lookup"><span data-stu-id="9c790-125">If you disable automated patching, Windows Update settings will not change.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c790-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="9c790-126">-InformationAction</span></span>
<span data-ttu-id="9c790-127">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="9c790-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="9c790-128">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="9c790-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9c790-129">持續</span><span class="sxs-lookup"><span data-stu-id="9c790-129">Continue</span></span>
- <span data-ttu-id="9c790-130">理會</span><span class="sxs-lookup"><span data-stu-id="9c790-130">Ignore</span></span>
- <span data-ttu-id="9c790-131">看</span><span class="sxs-lookup"><span data-stu-id="9c790-131">Inquire</span></span>
- <span data-ttu-id="9c790-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="9c790-132">SilentlyContinue</span></span>
- <span data-ttu-id="9c790-133">停止</span><span class="sxs-lookup"><span data-stu-id="9c790-133">Stop</span></span>
- <span data-ttu-id="9c790-134">封存</span><span class="sxs-lookup"><span data-stu-id="9c790-134">Suspend</span></span>

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

### <span data-ttu-id="9c790-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="9c790-135">-InformationVariable</span></span>
<span data-ttu-id="9c790-136">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="9c790-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="9c790-137">-MaintenanceWindowDuration</span><span class="sxs-lookup"><span data-stu-id="9c790-137">-MaintenanceWindowDuration</span></span>
<span data-ttu-id="9c790-138">指定 [維護] 視窗的持續時間。</span><span class="sxs-lookup"><span data-stu-id="9c790-138">Specifies the duration of the maintenance window.</span></span>
<span data-ttu-id="9c790-139">自動修補程式將避免執行可能會影響虛擬機器在該視窗以外可用性的動作。</span><span class="sxs-lookup"><span data-stu-id="9c790-139">Automated patching will avoid performing an action that can impact a virtual machine availability outside of that window.</span></span>
<span data-ttu-id="9c790-140">只允許30分鐘的增量。</span><span class="sxs-lookup"><span data-stu-id="9c790-140">Only 30 minutes increments are allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c790-141">-MaintenanceWindowStartingHour</span><span class="sxs-lookup"><span data-stu-id="9c790-141">-MaintenanceWindowStartingHour</span></span>
<span data-ttu-id="9c790-142">指定 [維護] 視窗啟動當天的小時。</span><span class="sxs-lookup"><span data-stu-id="9c790-142">Specifies the hour of the day when maintenance window starts.</span></span>
<span data-ttu-id="9c790-143">此時間定義更新開始安裝並四捨五入到小時的時機。</span><span class="sxs-lookup"><span data-stu-id="9c790-143">This time defines when updates start installing and is rounded to the hour.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c790-144">-PatchCategory</span><span class="sxs-lookup"><span data-stu-id="9c790-144">-PatchCategory</span></span>
<span data-ttu-id="9c790-145">指定是否應包含重要更新。</span><span class="sxs-lookup"><span data-stu-id="9c790-145">Specifies whether important updates should be included.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c790-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c790-146">CommonParameters</span></span>
<span data-ttu-id="9c790-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9c790-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c790-148">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9c790-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c790-149">輸入</span><span class="sxs-lookup"><span data-stu-id="9c790-149">INPUTS</span></span>

## <span data-ttu-id="9c790-150">輸出</span><span class="sxs-lookup"><span data-stu-id="9c790-150">OUTPUTS</span></span>

### <span data-ttu-id="9c790-151">AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="9c790-151">AutoPatchingSettings</span></span>
<span data-ttu-id="9c790-152">這個 Cmdlet 會傳回物件，其中包含自動修補程式的設定。</span><span class="sxs-lookup"><span data-stu-id="9c790-152">This cmdlet returns object contains settings for automated patching.</span></span>

## <span data-ttu-id="9c790-153">筆記</span><span class="sxs-lookup"><span data-stu-id="9c790-153">NOTES</span></span>

## <span data-ttu-id="9c790-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="9c790-154">RELATED LINKS</span></span>

[<span data-ttu-id="9c790-155">Set-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="9c790-155">Set-AzureVMSqlServerExtension</span></span>](./Set-AzureVMSqlServerExtension.md)

[<span data-ttu-id="9c790-156">移除-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="9c790-156">Remove-AzureVMSqlServerExtension</span></span>](./Remove-AzureVMSqlServerExtension.md)

[<span data-ttu-id="9c790-157">Set-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="9c790-157">Set-AzureVMSqlServerExtension</span></span>](./Set-AzureVMSqlServerExtension.md)


