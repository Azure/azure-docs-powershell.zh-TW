---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverautopatchingconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 0ce851373ac31aaef4c5664db7085f345e9b947d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93796106"
---
# <span data-ttu-id="3fb4a-101">New-AzVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="3fb4a-101">New-AzVMSqlServerAutoPatchingConfig</span></span>

## <span data-ttu-id="3fb4a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3fb4a-102">SYNOPSIS</span></span>
<span data-ttu-id="3fb4a-103">在虛擬機器上建立自動修補的設定物件。</span><span class="sxs-lookup"><span data-stu-id="3fb4a-103">Creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="3fb4a-104">句法</span><span class="sxs-lookup"><span data-stu-id="3fb4a-104">SYNTAX</span></span>

```
New-AzVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>]
 [-MaintenanceWindowStartingHour <Int32>] [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="3fb4a-105">說明</span><span class="sxs-lookup"><span data-stu-id="3fb4a-105">DESCRIPTION</span></span>
<span data-ttu-id="3fb4a-106">**新的-AzVMSqlServerAutoPatchingConfig** Cmdlet 會在虛擬機器上建立自動修補的設定物件。</span><span class="sxs-lookup"><span data-stu-id="3fb4a-106">The **New-AzVMSqlServerAutoPatchingConfig** cmdlet creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="3fb4a-107">示例</span><span class="sxs-lookup"><span data-stu-id="3fb4a-107">EXAMPLES</span></span>

### <span data-ttu-id="3fb4a-108">範例1：建立設定物件以設定自動修補</span><span class="sxs-lookup"><span data-stu-id="3fb4a-108">Example 1: Create a configuration object to configure automatic patching</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

<span data-ttu-id="3fb4a-109">這個命令會建立用來修補的設定物件。</span><span class="sxs-lookup"><span data-stu-id="3fb4a-109">This command creates configuration object for patching.</span></span>
<span data-ttu-id="3fb4a-110">該命令會指定一周中的一天，並定義 [維護] 視窗。</span><span class="sxs-lookup"><span data-stu-id="3fb4a-110">The command specifies the day of the week and defines the maintenance window.</span></span>
<span data-ttu-id="3fb4a-111">這項設定會啟用使用這些值的修補程式。</span><span class="sxs-lookup"><span data-stu-id="3fb4a-111">This configuration enables patching that uses these values.</span></span>
<span data-ttu-id="3fb4a-112">該命令會將結果儲存在 $AutoBackupConfig 變數中。</span><span class="sxs-lookup"><span data-stu-id="3fb4a-112">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="3fb4a-113">您可以為其他 Cmdlet 指定此設定專案，例如 Set-AzVMSqlServerExtension Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3fb4a-113">You can specify this configuration item for other cmdlets, such as the Set-AzVMSqlServerExtension cmdlet.</span></span>

## <span data-ttu-id="3fb4a-114">參數</span><span class="sxs-lookup"><span data-stu-id="3fb4a-114">PARAMETERS</span></span>

### <span data-ttu-id="3fb4a-115">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="3fb4a-115">-DayOfWeek</span></span>
<span data-ttu-id="3fb4a-116">指定一周中要安裝更新的日期。</span><span class="sxs-lookup"><span data-stu-id="3fb4a-116">Specifies the day of the week when updates should be installed.</span></span>

<span data-ttu-id="3fb4a-117">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="3fb4a-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3fb4a-118">日</span><span class="sxs-lookup"><span data-stu-id="3fb4a-118">Sunday</span></span>
- <span data-ttu-id="3fb4a-119">從</span><span class="sxs-lookup"><span data-stu-id="3fb4a-119">Monday</span></span>
- <span data-ttu-id="3fb4a-120">星期二</span><span class="sxs-lookup"><span data-stu-id="3fb4a-120">Tuesday</span></span>
- <span data-ttu-id="3fb4a-121">星期三</span><span class="sxs-lookup"><span data-stu-id="3fb4a-121">Wednesday</span></span>
- <span data-ttu-id="3fb4a-122">星期四</span><span class="sxs-lookup"><span data-stu-id="3fb4a-122">Thursday</span></span>
- <span data-ttu-id="3fb4a-123">日</span><span class="sxs-lookup"><span data-stu-id="3fb4a-123">Friday</span></span>
- <span data-ttu-id="3fb4a-124">星期六</span><span class="sxs-lookup"><span data-stu-id="3fb4a-124">Saturday</span></span>
- <span data-ttu-id="3fb4a-125">生活</span><span class="sxs-lookup"><span data-stu-id="3fb4a-125">Everyday</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Everyday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fb4a-126">-啟用</span><span class="sxs-lookup"><span data-stu-id="3fb4a-126">-Enable</span></span>
<span data-ttu-id="3fb4a-127">表示已啟用虛擬機器的自動修補程式。</span><span class="sxs-lookup"><span data-stu-id="3fb4a-127">Indicates that automated patching for the virtual machine is enabled.</span></span>
<span data-ttu-id="3fb4a-128">如果您啟用自動修補，則 Cmdlet 會將 Windows 更新放入互動模式。</span><span class="sxs-lookup"><span data-stu-id="3fb4a-128">If you enable automated patching the cmdlet puts Windows Update into interactive mode.</span></span>
<span data-ttu-id="3fb4a-129">如果您停用自動修補，Windows Update 設定就不會變更。</span><span class="sxs-lookup"><span data-stu-id="3fb4a-129">If you disable automated patching, Windows Update settings do not change.</span></span>

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

### <span data-ttu-id="3fb4a-130">-MaintenanceWindowDuration</span><span class="sxs-lookup"><span data-stu-id="3fb4a-130">-MaintenanceWindowDuration</span></span>
<span data-ttu-id="3fb4a-131">指定 [維護] 視窗的持續時間（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="3fb4a-131">Specifies the duration, in minutes, of the maintenance window.</span></span>
<span data-ttu-id="3fb4a-132">自動修補可避免執行可能會影響虛擬機器在該視窗以外的可用性的動作。</span><span class="sxs-lookup"><span data-stu-id="3fb4a-132">Automated patching avoids performing an action that can affect a virtual machine availability outside that window.</span></span>
<span data-ttu-id="3fb4a-133">指定30分鐘的倍數。</span><span class="sxs-lookup"><span data-stu-id="3fb4a-133">Specify a multiple of 30 minutes.</span></span>

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

### <span data-ttu-id="3fb4a-134">-MaintenanceWindowStartingHour</span><span class="sxs-lookup"><span data-stu-id="3fb4a-134">-MaintenanceWindowStartingHour</span></span>
<span data-ttu-id="3fb4a-135">指定 [維護] 視窗啟動當天的小時。</span><span class="sxs-lookup"><span data-stu-id="3fb4a-135">Specifies the hour of the day when maintenance window starts.</span></span>
<span data-ttu-id="3fb4a-136">此時間定義更新開始安裝的時機。</span><span class="sxs-lookup"><span data-stu-id="3fb4a-136">This time defines when updates start to install.</span></span>

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

### <span data-ttu-id="3fb4a-137">-PatchCategory</span><span class="sxs-lookup"><span data-stu-id="3fb4a-137">-PatchCategory</span></span>
<span data-ttu-id="3fb4a-138">指定是否應包含重要更新。</span><span class="sxs-lookup"><span data-stu-id="3fb4a-138">Specifies whether important updates should be included.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Important

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fb4a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fb4a-139">CommonParameters</span></span>
<span data-ttu-id="3fb4a-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3fb4a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fb4a-141">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3fb4a-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fb4a-142">輸入</span><span class="sxs-lookup"><span data-stu-id="3fb4a-142">INPUTS</span></span>

### <span data-ttu-id="3fb4a-143">所有</span><span class="sxs-lookup"><span data-stu-id="3fb4a-143">None</span></span>
<span data-ttu-id="3fb4a-144">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="3fb4a-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3fb4a-145">輸出</span><span class="sxs-lookup"><span data-stu-id="3fb4a-145">OUTPUTS</span></span>

### <span data-ttu-id="3fb4a-146">AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="3fb4a-146">AutoPatchingSettings</span></span>
<span data-ttu-id="3fb4a-147">這個 Cmdlet 會傳回物件，其中包含自動修補程式的設定。</span><span class="sxs-lookup"><span data-stu-id="3fb4a-147">This cmdlet returns object contains settings for automated patching.</span></span>

## <span data-ttu-id="3fb4a-148">筆記</span><span class="sxs-lookup"><span data-stu-id="3fb4a-148">NOTES</span></span>

## <span data-ttu-id="3fb4a-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="3fb4a-149">RELATED LINKS</span></span>

[<span data-ttu-id="3fb4a-150">新-AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="3fb4a-150">New-AzureVMSqlServerAutoBackupConfig</span></span>](./New-AzureVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="3fb4a-151">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="3fb4a-151">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


