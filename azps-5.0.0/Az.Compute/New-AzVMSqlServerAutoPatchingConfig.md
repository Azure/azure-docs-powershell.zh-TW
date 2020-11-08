---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverautopatchingconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 6fe89822af5be532674e22dd3e1c1edd583fced4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137174"
---
# <span data-ttu-id="0f75e-101">New-AzVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="0f75e-101">New-AzVMSqlServerAutoPatchingConfig</span></span>

## <span data-ttu-id="0f75e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0f75e-102">SYNOPSIS</span></span>
<span data-ttu-id="0f75e-103">在虛擬機器上建立自動修補的設定物件。</span><span class="sxs-lookup"><span data-stu-id="0f75e-103">Creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="0f75e-104">句法</span><span class="sxs-lookup"><span data-stu-id="0f75e-104">SYNTAX</span></span>

```
New-AzVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [<CommonParameters>]
```

## <span data-ttu-id="0f75e-105">說明</span><span class="sxs-lookup"><span data-stu-id="0f75e-105">DESCRIPTION</span></span>
<span data-ttu-id="0f75e-106">**新的-AzVMSqlServerAutoPatchingConfig** Cmdlet 會在虛擬機器上建立自動修補的設定物件。</span><span class="sxs-lookup"><span data-stu-id="0f75e-106">The **New-AzVMSqlServerAutoPatchingConfig** cmdlet creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="0f75e-107">示例</span><span class="sxs-lookup"><span data-stu-id="0f75e-107">EXAMPLES</span></span>

### <span data-ttu-id="0f75e-108">範例1：建立設定物件以設定自動修補</span><span class="sxs-lookup"><span data-stu-id="0f75e-108">Example 1: Create a configuration object to configure automatic patching</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

<span data-ttu-id="0f75e-109">這個命令會建立用來修補的設定物件。</span><span class="sxs-lookup"><span data-stu-id="0f75e-109">This command creates configuration object for patching.</span></span>
<span data-ttu-id="0f75e-110">該命令會指定一周中的一天，並定義 [維護] 視窗。</span><span class="sxs-lookup"><span data-stu-id="0f75e-110">The command specifies the day of the week and defines the maintenance window.</span></span>
<span data-ttu-id="0f75e-111">這項設定會啟用使用這些值的修補程式。</span><span class="sxs-lookup"><span data-stu-id="0f75e-111">This configuration enables patching that uses these values.</span></span>
<span data-ttu-id="0f75e-112">該命令會將結果儲存在 $AutoBackupConfig 變數中。</span><span class="sxs-lookup"><span data-stu-id="0f75e-112">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="0f75e-113">您可以為其他 Cmdlet 指定此設定專案，例如 Set-AzVMSqlServerExtension Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0f75e-113">You can specify this configuration item for other cmdlets, such as the Set-AzVMSqlServerExtension cmdlet.</span></span>

## <span data-ttu-id="0f75e-114">參數</span><span class="sxs-lookup"><span data-stu-id="0f75e-114">PARAMETERS</span></span>

### <span data-ttu-id="0f75e-115">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="0f75e-115">-DayOfWeek</span></span>
<span data-ttu-id="0f75e-116">指定一周中要安裝更新的日期。</span><span class="sxs-lookup"><span data-stu-id="0f75e-116">Specifies the day of the week when updates should be installed.</span></span>
<span data-ttu-id="0f75e-117">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="0f75e-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0f75e-118">日</span><span class="sxs-lookup"><span data-stu-id="0f75e-118">Sunday</span></span>
- <span data-ttu-id="0f75e-119">從</span><span class="sxs-lookup"><span data-stu-id="0f75e-119">Monday</span></span>
- <span data-ttu-id="0f75e-120">星期二</span><span class="sxs-lookup"><span data-stu-id="0f75e-120">Tuesday</span></span>
- <span data-ttu-id="0f75e-121">星期三</span><span class="sxs-lookup"><span data-stu-id="0f75e-121">Wednesday</span></span>
- <span data-ttu-id="0f75e-122">星期四</span><span class="sxs-lookup"><span data-stu-id="0f75e-122">Thursday</span></span>
- <span data-ttu-id="0f75e-123">日</span><span class="sxs-lookup"><span data-stu-id="0f75e-123">Friday</span></span>
- <span data-ttu-id="0f75e-124">星期六</span><span class="sxs-lookup"><span data-stu-id="0f75e-124">Saturday</span></span>
- <span data-ttu-id="0f75e-125">生活</span><span class="sxs-lookup"><span data-stu-id="0f75e-125">Everyday</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Everyday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f75e-126">-啟用</span><span class="sxs-lookup"><span data-stu-id="0f75e-126">-Enable</span></span>
<span data-ttu-id="0f75e-127">表示已啟用虛擬機器的自動修補程式。</span><span class="sxs-lookup"><span data-stu-id="0f75e-127">Indicates that automated patching for the virtual machine is enabled.</span></span>
<span data-ttu-id="0f75e-128">如果您啟用自動修補，則 Cmdlet 會將 Windows 更新放入互動模式。</span><span class="sxs-lookup"><span data-stu-id="0f75e-128">If you enable automated patching the cmdlet puts Windows Update into interactive mode.</span></span>
<span data-ttu-id="0f75e-129">如果您停用自動修補，Windows Update 設定就不會變更。</span><span class="sxs-lookup"><span data-stu-id="0f75e-129">If you disable automated patching, Windows Update settings do not change.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f75e-130">-MaintenanceWindowDuration</span><span class="sxs-lookup"><span data-stu-id="0f75e-130">-MaintenanceWindowDuration</span></span>
<span data-ttu-id="0f75e-131">指定 [維護] 視窗的持續時間（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="0f75e-131">Specifies the duration, in minutes, of the maintenance window.</span></span>
<span data-ttu-id="0f75e-132">自動修補可避免執行可能會影響虛擬機器在該視窗以外的可用性的動作。</span><span class="sxs-lookup"><span data-stu-id="0f75e-132">Automated patching avoids performing an action that can affect a virtual machine availability outside that window.</span></span>
<span data-ttu-id="0f75e-133">指定30分鐘的倍數。</span><span class="sxs-lookup"><span data-stu-id="0f75e-133">Specify a multiple of 30 minutes.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f75e-134">-MaintenanceWindowStartingHour</span><span class="sxs-lookup"><span data-stu-id="0f75e-134">-MaintenanceWindowStartingHour</span></span>
<span data-ttu-id="0f75e-135">指定 [維護] 視窗啟動當天的小時。</span><span class="sxs-lookup"><span data-stu-id="0f75e-135">Specifies the hour of the day when maintenance window starts.</span></span>
<span data-ttu-id="0f75e-136">此時間定義更新開始安裝的時機。</span><span class="sxs-lookup"><span data-stu-id="0f75e-136">This time defines when updates start to install.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f75e-137">-PatchCategory</span><span class="sxs-lookup"><span data-stu-id="0f75e-137">-PatchCategory</span></span>
<span data-ttu-id="0f75e-138">指定是否應包含重要更新。</span><span class="sxs-lookup"><span data-stu-id="0f75e-138">Specifies whether important updates should be included.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Important

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f75e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f75e-139">CommonParameters</span></span>
<span data-ttu-id="0f75e-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0f75e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f75e-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0f75e-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f75e-142">輸入</span><span class="sxs-lookup"><span data-stu-id="0f75e-142">INPUTS</span></span>

### <span data-ttu-id="0f75e-143">所有</span><span class="sxs-lookup"><span data-stu-id="0f75e-143">None</span></span>

## <span data-ttu-id="0f75e-144">輸出</span><span class="sxs-lookup"><span data-stu-id="0f75e-144">OUTPUTS</span></span>

### <span data-ttu-id="0f75e-145">AutoPatchingSettings 的計算。</span><span class="sxs-lookup"><span data-stu-id="0f75e-145">Microsoft.Azure.Commands.Compute.AutoPatchingSettings</span></span>

## <span data-ttu-id="0f75e-146">筆記</span><span class="sxs-lookup"><span data-stu-id="0f75e-146">NOTES</span></span>

## <span data-ttu-id="0f75e-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="0f75e-147">RELATED LINKS</span></span>

[<span data-ttu-id="0f75e-148">新-AzVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="0f75e-148">New-AzVMSqlServerAutoBackupConfig</span></span>](./New-AzVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="0f75e-149">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="0f75e-149">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


