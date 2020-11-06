---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
Module Name: Azure
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 17d99840bffb9063ad61dec00d4b7d5983118399
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456815"
---
# <span data-ttu-id="be85f-101">New-AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="be85f-101">New-AzureVMSqlServerAutoPatchingConfig</span></span>

## <span data-ttu-id="be85f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="be85f-102">SYNOPSIS</span></span>
<span data-ttu-id="be85f-103">在虛擬機器上建立自動修補的設定物件。</span><span class="sxs-lookup"><span data-stu-id="be85f-103">Creates a configuration object for automatic patching on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be85f-104">句法</span><span class="sxs-lookup"><span data-stu-id="be85f-104">SYNTAX</span></span>

```
New-AzureVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="be85f-105">說明</span><span class="sxs-lookup"><span data-stu-id="be85f-105">DESCRIPTION</span></span>
<span data-ttu-id="be85f-106">**新的-AzureVMSqlServerAutoPatchingConfig** Cmdlet 會在虛擬機器上建立自動修補的設定物件。</span><span class="sxs-lookup"><span data-stu-id="be85f-106">The **New-AzureVMSqlServerAutoPatchingConfig** cmdlet creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="be85f-107">示例</span><span class="sxs-lookup"><span data-stu-id="be85f-107">EXAMPLES</span></span>

### <span data-ttu-id="be85f-108">範例1：建立設定物件以設定自動修補</span><span class="sxs-lookup"><span data-stu-id="be85f-108">Example 1: Create a configuration object to configure automatic patching</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

<span data-ttu-id="be85f-109">這個命令會建立用來修補的設定物件。</span><span class="sxs-lookup"><span data-stu-id="be85f-109">This command creates configuration object for patching.</span></span>
<span data-ttu-id="be85f-110">該命令會指定一周中的一天，並定義 [維護] 視窗。</span><span class="sxs-lookup"><span data-stu-id="be85f-110">The command specifies the day of the week and defines the maintenance window.</span></span>
<span data-ttu-id="be85f-111">這項設定會啟用使用這些值的修補程式。</span><span class="sxs-lookup"><span data-stu-id="be85f-111">This configuration enables patching that uses these values.</span></span>
<span data-ttu-id="be85f-112">該命令會將結果儲存在 $AutoBackupConfig 變數中。</span><span class="sxs-lookup"><span data-stu-id="be85f-112">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="be85f-113">您可以為其他 Cmdlet 指定此設定專案，例如 Set-AzureRmVMSqlServerExtension Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="be85f-113">You can specify this configuration item for other cmdlets, such as the Set-AzureRmVMSqlServerExtension cmdlet.</span></span>

## <span data-ttu-id="be85f-114">參數</span><span class="sxs-lookup"><span data-stu-id="be85f-114">PARAMETERS</span></span>

### <span data-ttu-id="be85f-115">-啟用</span><span class="sxs-lookup"><span data-stu-id="be85f-115">-Enable</span></span>
<span data-ttu-id="be85f-116">表示已啟用虛擬機器的自動修補程式。</span><span class="sxs-lookup"><span data-stu-id="be85f-116">Indicates that automated patching for the virtual machine is enabled.</span></span>
<span data-ttu-id="be85f-117">如果您啟用自動修補，則 Cmdlet 會將 Windows 更新放入互動模式。</span><span class="sxs-lookup"><span data-stu-id="be85f-117">If you enable automated patching the cmdlet puts Windows Update into interactive mode.</span></span>
<span data-ttu-id="be85f-118">如果您停用自動修補，Windows Update 設定就不會變更。</span><span class="sxs-lookup"><span data-stu-id="be85f-118">If you disable automated patching, Windows Update settings do not change.</span></span>

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

### <span data-ttu-id="be85f-119">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="be85f-119">-DayOfWeek</span></span>
<span data-ttu-id="be85f-120">指定一周中要安裝更新的日期。</span><span class="sxs-lookup"><span data-stu-id="be85f-120">Specifies the day of the week when updates should be installed.</span></span>

<span data-ttu-id="be85f-121">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="be85f-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="be85f-122">日</span><span class="sxs-lookup"><span data-stu-id="be85f-122">Sunday</span></span>
- <span data-ttu-id="be85f-123">從</span><span class="sxs-lookup"><span data-stu-id="be85f-123">Monday</span></span>
- <span data-ttu-id="be85f-124">星期二</span><span class="sxs-lookup"><span data-stu-id="be85f-124">Tuesday</span></span>
- <span data-ttu-id="be85f-125">星期三</span><span class="sxs-lookup"><span data-stu-id="be85f-125">Wednesday</span></span>
- <span data-ttu-id="be85f-126">星期四</span><span class="sxs-lookup"><span data-stu-id="be85f-126">Thursday</span></span>
- <span data-ttu-id="be85f-127">日</span><span class="sxs-lookup"><span data-stu-id="be85f-127">Friday</span></span>
- <span data-ttu-id="be85f-128">星期六</span><span class="sxs-lookup"><span data-stu-id="be85f-128">Saturday</span></span>
- <span data-ttu-id="be85f-129">生活</span><span class="sxs-lookup"><span data-stu-id="be85f-129">Everyday</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be85f-130">-MaintenanceWindowStartingHour</span><span class="sxs-lookup"><span data-stu-id="be85f-130">-MaintenanceWindowStartingHour</span></span>
<span data-ttu-id="be85f-131">指定 [維護] 視窗啟動當天的小時。</span><span class="sxs-lookup"><span data-stu-id="be85f-131">Specifies the hour of the day when maintenance window starts.</span></span>
<span data-ttu-id="be85f-132">此時間定義更新開始安裝的時機。</span><span class="sxs-lookup"><span data-stu-id="be85f-132">This time defines when updates start to install.</span></span>

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

### <span data-ttu-id="be85f-133">-MaintenanceWindowDuration</span><span class="sxs-lookup"><span data-stu-id="be85f-133">-MaintenanceWindowDuration</span></span>
<span data-ttu-id="be85f-134">指定 [維護] 視窗的持續時間（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="be85f-134">Specifies the duration, in minutes, of the maintenance window.</span></span>
<span data-ttu-id="be85f-135">自動修補可避免執行可能會影響虛擬機器在該視窗以外的可用性的動作。</span><span class="sxs-lookup"><span data-stu-id="be85f-135">Automated patching avoids performing an action that can affect a virtual machine availability outside that window.</span></span>
<span data-ttu-id="be85f-136">指定30分鐘的倍數。</span><span class="sxs-lookup"><span data-stu-id="be85f-136">Specify a multiple of 30 minutes.</span></span>

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

### <span data-ttu-id="be85f-137">-PatchCategory</span><span class="sxs-lookup"><span data-stu-id="be85f-137">-PatchCategory</span></span>
<span data-ttu-id="be85f-138">指定是否應包含重要更新。</span><span class="sxs-lookup"><span data-stu-id="be85f-138">Specifies whether important updates should be included.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be85f-139">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="be85f-139">-InformationAction</span></span>
<span data-ttu-id="be85f-140">@ {Text =}</span><span class="sxs-lookup"><span data-stu-id="be85f-140">@{Text=}</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be85f-141">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="be85f-141">-InformationVariable</span></span>
<span data-ttu-id="be85f-142">@ {Text =}</span><span class="sxs-lookup"><span data-stu-id="be85f-142">@{Text=}</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be85f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be85f-143">CommonParameters</span></span>
<span data-ttu-id="be85f-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="be85f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be85f-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="be85f-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be85f-146">輸入</span><span class="sxs-lookup"><span data-stu-id="be85f-146">INPUTS</span></span>

## <span data-ttu-id="be85f-147">輸出</span><span class="sxs-lookup"><span data-stu-id="be85f-147">OUTPUTS</span></span>

### <span data-ttu-id="be85f-148">AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="be85f-148">AutoPatchingSettings</span></span>
<span data-ttu-id="be85f-149">這個 Cmdlet 會傳回物件，其中包含自動修補程式的設定。</span><span class="sxs-lookup"><span data-stu-id="be85f-149">This cmdlet returns object contains settings for automated patching.</span></span>

## <span data-ttu-id="be85f-150">筆記</span><span class="sxs-lookup"><span data-stu-id="be85f-150">NOTES</span></span>

## <span data-ttu-id="be85f-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="be85f-151">RELATED LINKS</span></span>

[<span data-ttu-id="be85f-152">新-AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="be85f-152">New-AzureVMSqlServerAutoBackupConfig</span></span>](./New-AzureVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="be85f-153">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="be85f-153">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


