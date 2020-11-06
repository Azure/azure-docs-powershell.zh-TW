---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverautopatchingconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 302197adbbf6e90397a5bb6f3e96be6d6836b1bf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613294"
---
# <span data-ttu-id="7d1ca-101">New-AzVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="7d1ca-101">New-AzVMSqlServerAutoPatchingConfig</span></span>

## <span data-ttu-id="7d1ca-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7d1ca-102">SYNOPSIS</span></span>
<span data-ttu-id="7d1ca-103">在虛擬機器上建立自動修補的設定物件。</span><span class="sxs-lookup"><span data-stu-id="7d1ca-103">Creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="7d1ca-104">句法</span><span class="sxs-lookup"><span data-stu-id="7d1ca-104">SYNTAX</span></span>

```
New-AzVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [<CommonParameters>]
```

## <span data-ttu-id="7d1ca-105">說明</span><span class="sxs-lookup"><span data-stu-id="7d1ca-105">DESCRIPTION</span></span>
<span data-ttu-id="7d1ca-106">**新的-AzVMSqlServerAutoPatchingConfig** Cmdlet 會在虛擬機器上建立自動修補的設定物件。</span><span class="sxs-lookup"><span data-stu-id="7d1ca-106">The **New-AzVMSqlServerAutoPatchingConfig** cmdlet creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="7d1ca-107">示例</span><span class="sxs-lookup"><span data-stu-id="7d1ca-107">EXAMPLES</span></span>

### <span data-ttu-id="7d1ca-108">範例1：建立設定物件以設定自動修補</span><span class="sxs-lookup"><span data-stu-id="7d1ca-108">Example 1: Create a configuration object to configure automatic patching</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

<span data-ttu-id="7d1ca-109">這個命令會建立用來修補的設定物件。</span><span class="sxs-lookup"><span data-stu-id="7d1ca-109">This command creates configuration object for patching.</span></span>
<span data-ttu-id="7d1ca-110">該命令會指定一周中的一天，並定義 [維護] 視窗。</span><span class="sxs-lookup"><span data-stu-id="7d1ca-110">The command specifies the day of the week and defines the maintenance window.</span></span>
<span data-ttu-id="7d1ca-111">這項設定會啟用使用這些值的修補程式。</span><span class="sxs-lookup"><span data-stu-id="7d1ca-111">This configuration enables patching that uses these values.</span></span>
<span data-ttu-id="7d1ca-112">該命令會將結果儲存在 $AutoBackupConfig 變數中。</span><span class="sxs-lookup"><span data-stu-id="7d1ca-112">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="7d1ca-113">您可以為其他 Cmdlet 指定此設定專案，例如 Set-AzVMSqlServerExtension Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7d1ca-113">You can specify this configuration item for other cmdlets, such as the Set-AzVMSqlServerExtension cmdlet.</span></span>

## <span data-ttu-id="7d1ca-114">參數</span><span class="sxs-lookup"><span data-stu-id="7d1ca-114">PARAMETERS</span></span>

### <span data-ttu-id="7d1ca-115">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="7d1ca-115">-DayOfWeek</span></span>
<span data-ttu-id="7d1ca-116">指定一周中要安裝更新的日期。</span><span class="sxs-lookup"><span data-stu-id="7d1ca-116">Specifies the day of the week when updates should be installed.</span></span>
<span data-ttu-id="7d1ca-117">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="7d1ca-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7d1ca-118">日</span><span class="sxs-lookup"><span data-stu-id="7d1ca-118">Sunday</span></span>
- <span data-ttu-id="7d1ca-119">從</span><span class="sxs-lookup"><span data-stu-id="7d1ca-119">Monday</span></span>
- <span data-ttu-id="7d1ca-120">星期二</span><span class="sxs-lookup"><span data-stu-id="7d1ca-120">Tuesday</span></span>
- <span data-ttu-id="7d1ca-121">星期三</span><span class="sxs-lookup"><span data-stu-id="7d1ca-121">Wednesday</span></span>
- <span data-ttu-id="7d1ca-122">星期四</span><span class="sxs-lookup"><span data-stu-id="7d1ca-122">Thursday</span></span>
- <span data-ttu-id="7d1ca-123">日</span><span class="sxs-lookup"><span data-stu-id="7d1ca-123">Friday</span></span>
- <span data-ttu-id="7d1ca-124">星期六</span><span class="sxs-lookup"><span data-stu-id="7d1ca-124">Saturday</span></span>
- <span data-ttu-id="7d1ca-125">生活</span><span class="sxs-lookup"><span data-stu-id="7d1ca-125">Everyday</span></span>

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

### <span data-ttu-id="7d1ca-126">-啟用</span><span class="sxs-lookup"><span data-stu-id="7d1ca-126">-Enable</span></span>
<span data-ttu-id="7d1ca-127">表示已啟用虛擬機器的自動修補程式。</span><span class="sxs-lookup"><span data-stu-id="7d1ca-127">Indicates that automated patching for the virtual machine is enabled.</span></span>
<span data-ttu-id="7d1ca-128">如果您啟用自動修補，則 Cmdlet 會將 Windows 更新放入互動模式。</span><span class="sxs-lookup"><span data-stu-id="7d1ca-128">If you enable automated patching the cmdlet puts Windows Update into interactive mode.</span></span>
<span data-ttu-id="7d1ca-129">如果您停用自動修補，Windows Update 設定就不會變更。</span><span class="sxs-lookup"><span data-stu-id="7d1ca-129">If you disable automated patching, Windows Update settings do not change.</span></span>

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

### <span data-ttu-id="7d1ca-130">-MaintenanceWindowDuration</span><span class="sxs-lookup"><span data-stu-id="7d1ca-130">-MaintenanceWindowDuration</span></span>
<span data-ttu-id="7d1ca-131">指定 [維護] 視窗的持續時間（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="7d1ca-131">Specifies the duration, in minutes, of the maintenance window.</span></span>
<span data-ttu-id="7d1ca-132">自動修補可避免執行可能會影響虛擬機器在該視窗以外的可用性的動作。</span><span class="sxs-lookup"><span data-stu-id="7d1ca-132">Automated patching avoids performing an action that can affect a virtual machine availability outside that window.</span></span>
<span data-ttu-id="7d1ca-133">指定30分鐘的倍數。</span><span class="sxs-lookup"><span data-stu-id="7d1ca-133">Specify a multiple of 30 minutes.</span></span>

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

### <span data-ttu-id="7d1ca-134">-MaintenanceWindowStartingHour</span><span class="sxs-lookup"><span data-stu-id="7d1ca-134">-MaintenanceWindowStartingHour</span></span>
<span data-ttu-id="7d1ca-135">指定 [維護] 視窗啟動當天的小時。</span><span class="sxs-lookup"><span data-stu-id="7d1ca-135">Specifies the hour of the day when maintenance window starts.</span></span>
<span data-ttu-id="7d1ca-136">此時間定義更新開始安裝的時機。</span><span class="sxs-lookup"><span data-stu-id="7d1ca-136">This time defines when updates start to install.</span></span>

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

### <span data-ttu-id="7d1ca-137">-PatchCategory</span><span class="sxs-lookup"><span data-stu-id="7d1ca-137">-PatchCategory</span></span>
<span data-ttu-id="7d1ca-138">指定是否應包含重要更新。</span><span class="sxs-lookup"><span data-stu-id="7d1ca-138">Specifies whether important updates should be included.</span></span>

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

### <span data-ttu-id="7d1ca-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d1ca-139">CommonParameters</span></span>
<span data-ttu-id="7d1ca-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7d1ca-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d1ca-141">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7d1ca-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d1ca-142">輸入</span><span class="sxs-lookup"><span data-stu-id="7d1ca-142">INPUTS</span></span>

### <span data-ttu-id="7d1ca-143">所有</span><span class="sxs-lookup"><span data-stu-id="7d1ca-143">None</span></span>

## <span data-ttu-id="7d1ca-144">輸出</span><span class="sxs-lookup"><span data-stu-id="7d1ca-144">OUTPUTS</span></span>

### <span data-ttu-id="7d1ca-145">AutoPatchingSettings 的計算。</span><span class="sxs-lookup"><span data-stu-id="7d1ca-145">Microsoft.Azure.Commands.Compute.AutoPatchingSettings</span></span>

## <span data-ttu-id="7d1ca-146">筆記</span><span class="sxs-lookup"><span data-stu-id="7d1ca-146">NOTES</span></span>

## <span data-ttu-id="7d1ca-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="7d1ca-147">RELATED LINKS</span></span>

[<span data-ttu-id="7d1ca-148">新-AzVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="7d1ca-148">New-AzVMSqlServerAutoBackupConfig</span></span>](./New-AzVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="7d1ca-149">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="7d1ca-149">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


