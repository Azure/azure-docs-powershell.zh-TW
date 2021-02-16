---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverautopatchingconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 3ba7ab00076a3a0634a0d4394270fe4a83ec8ede
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398252"
---
# <span data-ttu-id="41d9d-101">New-AzVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="41d9d-101">New-AzVMSqlServerAutoPatchingConfig</span></span>

## <span data-ttu-id="41d9d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="41d9d-102">SYNOPSIS</span></span>
<span data-ttu-id="41d9d-103">建立虛擬機器上自動修補的組塊物件。</span><span class="sxs-lookup"><span data-stu-id="41d9d-103">Creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="41d9d-104">語法</span><span class="sxs-lookup"><span data-stu-id="41d9d-104">SYNTAX</span></span>

```
New-AzVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>]
 [-MaintenanceWindowStartingHour <Int32>] [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="41d9d-105">描述</span><span class="sxs-lookup"><span data-stu-id="41d9d-105">DESCRIPTION</span></span>
<span data-ttu-id="41d9d-106">**New-AzMSqlServerAutoPatchingConfig** Cmdlet 會建立一個組塊物件，以在虛擬機器上自動修補。</span><span class="sxs-lookup"><span data-stu-id="41d9d-106">The **New-AzVMSqlServerAutoPatchingConfig** cmdlet creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="41d9d-107">例子</span><span class="sxs-lookup"><span data-stu-id="41d9d-107">EXAMPLES</span></span>

### <span data-ttu-id="41d9d-108">範例 1：建立設定物件以設定自動修補</span><span class="sxs-lookup"><span data-stu-id="41d9d-108">Example 1: Create a configuration object to configure automatic patching</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

<span data-ttu-id="41d9d-109">此命令會建立修補的組塊物件。</span><span class="sxs-lookup"><span data-stu-id="41d9d-109">This command creates configuration object for patching.</span></span>
<span data-ttu-id="41d9d-110">命令會指定一周中的星期，並定義維護視窗。</span><span class="sxs-lookup"><span data-stu-id="41d9d-110">The command specifies the day of the week and defines the maintenance window.</span></span>
<span data-ttu-id="41d9d-111">此組塊可啟用使用這些值的修補。</span><span class="sxs-lookup"><span data-stu-id="41d9d-111">This configuration enables patching that uses these values.</span></span>
<span data-ttu-id="41d9d-112">該命令會將結果儲存在$AutoBackupConfig變數中。</span><span class="sxs-lookup"><span data-stu-id="41d9d-112">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="41d9d-113">您可以為其他 Cmdlet 指定此組Set-AzVMSqlServerExtension專案。</span><span class="sxs-lookup"><span data-stu-id="41d9d-113">You can specify this configuration item for other cmdlets, such as the Set-AzVMSqlServerExtension cmdlet.</span></span>

## <span data-ttu-id="41d9d-114">參數</span><span class="sxs-lookup"><span data-stu-id="41d9d-114">PARAMETERS</span></span>

### <span data-ttu-id="41d9d-115">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="41d9d-115">-DayOfWeek</span></span>
<span data-ttu-id="41d9d-116">指定一周中應該安裝更新的日子。</span><span class="sxs-lookup"><span data-stu-id="41d9d-116">Specifies the day of the week when updates should be installed.</span></span>

<span data-ttu-id="41d9d-117">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="41d9d-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="41d9d-118">星期天</span><span class="sxs-lookup"><span data-stu-id="41d9d-118">Sunday</span></span>
- <span data-ttu-id="41d9d-119">星期一</span><span class="sxs-lookup"><span data-stu-id="41d9d-119">Monday</span></span>
- <span data-ttu-id="41d9d-120">星期二</span><span class="sxs-lookup"><span data-stu-id="41d9d-120">Tuesday</span></span>
- <span data-ttu-id="41d9d-121">星期三</span><span class="sxs-lookup"><span data-stu-id="41d9d-121">Wednesday</span></span>
- <span data-ttu-id="41d9d-122">星期四</span><span class="sxs-lookup"><span data-stu-id="41d9d-122">Thursday</span></span>
- <span data-ttu-id="41d9d-123">星期五</span><span class="sxs-lookup"><span data-stu-id="41d9d-123">Friday</span></span>
- <span data-ttu-id="41d9d-124">星期六</span><span class="sxs-lookup"><span data-stu-id="41d9d-124">Saturday</span></span>
- <span data-ttu-id="41d9d-125">每天</span><span class="sxs-lookup"><span data-stu-id="41d9d-125">Everyday</span></span>

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

### <span data-ttu-id="41d9d-126">-啟用</span><span class="sxs-lookup"><span data-stu-id="41d9d-126">-Enable</span></span>
<span data-ttu-id="41d9d-127">表示已啟用虛擬機器的自動修補功能。</span><span class="sxs-lookup"><span data-stu-id="41d9d-127">Indicates that automated patching for the virtual machine is enabled.</span></span>
<span data-ttu-id="41d9d-128">如果您啟用自動修補，Cmdlet 會將 Windows Update 進入互動式模式。</span><span class="sxs-lookup"><span data-stu-id="41d9d-128">If you enable automated patching the cmdlet puts Windows Update into interactive mode.</span></span>
<span data-ttu-id="41d9d-129">如果您停用自動修補，Windows Update 設定不會變更。</span><span class="sxs-lookup"><span data-stu-id="41d9d-129">If you disable automated patching, Windows Update settings do not change.</span></span>

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

### <span data-ttu-id="41d9d-130">-MaintenanceWindowDuration</span><span class="sxs-lookup"><span data-stu-id="41d9d-130">-MaintenanceWindowDuration</span></span>
<span data-ttu-id="41d9d-131">指定維護視窗的工期 ，以分鐘表示。</span><span class="sxs-lookup"><span data-stu-id="41d9d-131">Specifies the duration, in minutes, of the maintenance window.</span></span>
<span data-ttu-id="41d9d-132">自動修補可避免執行可能會影響該視窗外部虛擬機器可用性的動作。</span><span class="sxs-lookup"><span data-stu-id="41d9d-132">Automated patching avoids performing an action that can affect a virtual machine availability outside that window.</span></span>
<span data-ttu-id="41d9d-133">指定 30 分鐘的倍數。</span><span class="sxs-lookup"><span data-stu-id="41d9d-133">Specify a multiple of 30 minutes.</span></span>

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

### <span data-ttu-id="41d9d-134">-MaintenanceWindowStartingHour</span><span class="sxs-lookup"><span data-stu-id="41d9d-134">-MaintenanceWindowStartingHour</span></span>
<span data-ttu-id="41d9d-135">指定維護視窗啟動時的一天中小時。</span><span class="sxs-lookup"><span data-stu-id="41d9d-135">Specifies the hour of the day when maintenance window starts.</span></span>
<span data-ttu-id="41d9d-136">這次會定義何時開始安裝更新。</span><span class="sxs-lookup"><span data-stu-id="41d9d-136">This time defines when updates start to install.</span></span>

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

### <span data-ttu-id="41d9d-137">-PatchCategory</span><span class="sxs-lookup"><span data-stu-id="41d9d-137">-PatchCategory</span></span>
<span data-ttu-id="41d9d-138">指定是否應該包含重要的更新。</span><span class="sxs-lookup"><span data-stu-id="41d9d-138">Specifies whether important updates should be included.</span></span>

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

### <span data-ttu-id="41d9d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41d9d-139">CommonParameters</span></span>
<span data-ttu-id="41d9d-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="41d9d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41d9d-141">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="41d9d-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41d9d-142">輸入</span><span class="sxs-lookup"><span data-stu-id="41d9d-142">INPUTS</span></span>

### <span data-ttu-id="41d9d-143">沒有</span><span class="sxs-lookup"><span data-stu-id="41d9d-143">None</span></span>
<span data-ttu-id="41d9d-144">此 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="41d9d-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="41d9d-145">輸出</span><span class="sxs-lookup"><span data-stu-id="41d9d-145">OUTPUTS</span></span>

### <span data-ttu-id="41d9d-146">自動修補設定</span><span class="sxs-lookup"><span data-stu-id="41d9d-146">AutoPatchingSettings</span></span>
<span data-ttu-id="41d9d-147">此 Cmdlet 會返回包含自動修補設定的物件。</span><span class="sxs-lookup"><span data-stu-id="41d9d-147">This cmdlet returns object contains settings for automated patching.</span></span>

## <span data-ttu-id="41d9d-148">筆記</span><span class="sxs-lookup"><span data-stu-id="41d9d-148">NOTES</span></span>

## <span data-ttu-id="41d9d-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="41d9d-149">RELATED LINKS</span></span>

[<span data-ttu-id="41d9d-150">New-AzureMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="41d9d-150">New-AzureVMSqlServerAutoBackupConfig</span></span>](./New-AzVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="41d9d-151">Set-AzMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="41d9d-151">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


