---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restore-azdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzDeletedWebApp.md
ms.openlocfilehash: a413c0b021a167252469f211b5a8e5af670f9ff0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93793007"
---
# <span data-ttu-id="91145-101">Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="91145-101">Restore-AzDeletedWebApp</span></span>

## <span data-ttu-id="91145-102">摘要</span><span class="sxs-lookup"><span data-stu-id="91145-102">SYNOPSIS</span></span>
<span data-ttu-id="91145-103">將已刪除的 web 應用程式還原到新的或現有的 web 應用程式。</span><span class="sxs-lookup"><span data-stu-id="91145-103">Restores a deleted web app to a new or existing web app.</span></span>

## <span data-ttu-id="91145-104">句法</span><span class="sxs-lookup"><span data-stu-id="91145-104">SYNTAX</span></span>

### <span data-ttu-id="91145-105">FromDeletedResourceName (預設) </span><span class="sxs-lookup"><span data-stu-id="91145-105">FromDeletedResourceName (Default)</span></span>
```
Restore-AzDeletedWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-Location <String>]
 [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-UseDisasterRecovery] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91145-106">FromDeletedApp</span><span class="sxs-lookup"><span data-stu-id="91145-106">FromDeletedApp</span></span>
```
Restore-AzDeletedWebApp [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-UseDisasterRecovery] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-InputObject] <PSAzureDeletedWebApp> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="91145-107">說明</span><span class="sxs-lookup"><span data-stu-id="91145-107">DESCRIPTION</span></span>
<span data-ttu-id="91145-108">**Restore-AzDeletedWebApp** Cmdlet 會還原已刪除的 web 應用程式。</span><span class="sxs-lookup"><span data-stu-id="91145-108">The **Restore-AzDeletedWebApp** cmdlet restores a deleted web app.</span></span> <span data-ttu-id="91145-109">TargetResourceGroupName、TargetName 和 TargetSlot 所指定的 web app 將會覆寫已刪除 web 應用程式的內容和設定。</span><span class="sxs-lookup"><span data-stu-id="91145-109">The web app specified by TargetResourceGroupName, TargetName, and TargetSlot will be overwritten with the contents and settings of the deleted web app.</span></span> <span data-ttu-id="91145-110">如果未指定目標參數，則會自動使用已刪除的 web 應用程式的資源群組、名稱和槽來填入它們。</span><span class="sxs-lookup"><span data-stu-id="91145-110">If the target parameters are not specified, they will automatically be filled with the deleted web app's resource group, name, and slot.</span></span> <span data-ttu-id="91145-111">如果目標 web 應用程式不存在，則會自動在 TargetAppServicePlanName 指定的 app 服務方案中建立它。</span><span class="sxs-lookup"><span data-stu-id="91145-111">If the target web app does not exist, it will automatically be created in the app service plan specified by TargetAppServicePlanName.</span></span> <span data-ttu-id="91145-112">RestoreContentOnly 切換參數只能用來還原已刪除 app 的檔案，而不需要 app 設定。</span><span class="sxs-lookup"><span data-stu-id="91145-112">The RestoreContentOnly switch parameter can be used to restore only the deleted app's files without the app settings.</span></span>

## <span data-ttu-id="91145-113">示例</span><span class="sxs-lookup"><span data-stu-id="91145-113">EXAMPLES</span></span>

### <span data-ttu-id="91145-114">範例1</span><span class="sxs-lookup"><span data-stu-id="91145-114">Example 1</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -TargetAppServicePlanName ContosoPlan
```

<span data-ttu-id="91145-115">還原名為 ContosoApp 的已刪除應用程式，其名稱為「資源群組預設-Web-WestUS」。</span><span class="sxs-lookup"><span data-stu-id="91145-115">Restores a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="91145-116">將會在名為 ContosoPlan 的應用程式服務方案中建立具有相同名稱和資源群組的新應用程式，並將已刪除的應用程式的檔案和設定還原到其中。</span><span class="sxs-lookup"><span data-stu-id="91145-116">A new app with the same name and resource group will be created in the App Service Plan named ContosoPlan, and the deleted app's files and settings will be restored to it.</span></span>

### <span data-ttu-id="91145-117">範例2</span><span class="sxs-lookup"><span data-stu-id="91145-117">Example 2</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -Slot Staging -TargetResourceGroupName Default-Web-EastUS -TargetName ContosoRestore -RestoreContentOnly
```

<span data-ttu-id="91145-118">還原名為 ContosoApp 的已刪除應用程式的暫存槽，其名稱為「資源群組預設-WestUS」。</span><span class="sxs-lookup"><span data-stu-id="91145-118">Restores the Staging slot of a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="91145-119">ContosoRestore 屬於資源群組的 web app （預設為 [網頁-EastUS]）將會被覆蓋。</span><span class="sxs-lookup"><span data-stu-id="91145-119">The web app named ContosoRestore belonging to the resource group Default-Web-EastUS will be overwritten.</span></span> <span data-ttu-id="91145-120">已刪除的 web 應用程式設定將無法還原。</span><span class="sxs-lookup"><span data-stu-id="91145-120">The deleted web app settings will not be restored.</span></span>

## <span data-ttu-id="91145-121">參數</span><span class="sxs-lookup"><span data-stu-id="91145-121">PARAMETERS</span></span>

### <span data-ttu-id="91145-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="91145-122">-AsJob</span></span>
<span data-ttu-id="91145-123">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="91145-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="91145-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91145-124">-DefaultProfile</span></span>
<span data-ttu-id="91145-125">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="91145-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91145-126">-Force</span><span class="sxs-lookup"><span data-stu-id="91145-126">-Force</span></span>
<span data-ttu-id="91145-127">在不提示確認的情況下執行還原。</span><span class="sxs-lookup"><span data-stu-id="91145-127">Do the restore without prompting for confirmation.</span></span>

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

### <span data-ttu-id="91145-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="91145-128">-InputObject</span></span>
<span data-ttu-id="91145-129">已刪除的 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="91145-129">The deleted Azure Web App.</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp
Parameter Sets: FromDeletedApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="91145-130">-位置</span><span class="sxs-lookup"><span data-stu-id="91145-130">-Location</span></span>
<span data-ttu-id="91145-131">已刪除的 Azure Web App 的位置。</span><span class="sxs-lookup"><span data-stu-id="91145-131">The location of the deleted Azure Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91145-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="91145-132">-Name</span></span>
<span data-ttu-id="91145-133">已刪除的 Azure Web 應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="91145-133">The name of the deleted Azure Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91145-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91145-134">-ResourceGroupName</span></span>
<span data-ttu-id="91145-135">已刪除的 Azure Web App 的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="91145-135">The resource group of the deleted Azure Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91145-136">-RestoreContentOnly</span><span class="sxs-lookup"><span data-stu-id="91145-136">-RestoreContentOnly</span></span>
<span data-ttu-id="91145-137">還原 web 應用程式的檔案，但不要還原設定。</span><span class="sxs-lookup"><span data-stu-id="91145-137">Restore the web app's files, but do not restore the settings.</span></span>

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

### <span data-ttu-id="91145-138">-槽</span><span class="sxs-lookup"><span data-stu-id="91145-138">-Slot</span></span>
<span data-ttu-id="91145-139">已刪除的 Azure Web App 槽。</span><span class="sxs-lookup"><span data-stu-id="91145-139">The deleted Azure Web App slot.</span></span>

```yaml
Type: System.String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91145-140">-TargetAppServicePlanName</span><span class="sxs-lookup"><span data-stu-id="91145-140">-TargetAppServicePlanName</span></span>
<span data-ttu-id="91145-141">新 Azure Web App 的 App 服務規劃。</span><span class="sxs-lookup"><span data-stu-id="91145-141">The App Service Plan for the new Azure Web App.</span></span>

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

### <span data-ttu-id="91145-142">-TargetName</span><span class="sxs-lookup"><span data-stu-id="91145-142">-TargetName</span></span>
<span data-ttu-id="91145-143">新的 Azure Web App 名稱。</span><span class="sxs-lookup"><span data-stu-id="91145-143">The name of the new Azure Web App.</span></span>

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

### <span data-ttu-id="91145-144">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91145-144">-TargetResourceGroupName</span></span>
<span data-ttu-id="91145-145">包含新 Azure Web App 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="91145-145">The resource group containing the new Azure Web App.</span></span>

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

### <span data-ttu-id="91145-146">-TargetSlot</span><span class="sxs-lookup"><span data-stu-id="91145-146">-TargetSlot</span></span>
<span data-ttu-id="91145-147">新的 Azure Web App 槽的名稱。</span><span class="sxs-lookup"><span data-stu-id="91145-147">The name of the new Azure Web App slot.</span></span>

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

### <span data-ttu-id="91145-148">-UseDisasterRecovery</span><span class="sxs-lookup"><span data-stu-id="91145-148">-UseDisasterRecovery</span></span>
<span data-ttu-id="91145-149">用來從離線的縮放單位復原已刪除的 app。</span><span class="sxs-lookup"><span data-stu-id="91145-149">Use to recover a deleted app from a scale unit that is offline.</span></span>

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

### <span data-ttu-id="91145-150">-確認</span><span class="sxs-lookup"><span data-stu-id="91145-150">-Confirm</span></span>
<span data-ttu-id="91145-151">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="91145-151">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91145-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91145-152">-WhatIf</span></span>
<span data-ttu-id="91145-153">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="91145-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="91145-154">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="91145-154">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91145-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91145-155">CommonParameters</span></span>
<span data-ttu-id="91145-156">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="91145-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91145-157">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="91145-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91145-158">輸入</span><span class="sxs-lookup"><span data-stu-id="91145-158">INPUTS</span></span>

### <span data-ttu-id="91145-159">WebApps WebApps. PSAzureDeletedWebApp （）</span><span class="sxs-lookup"><span data-stu-id="91145-159">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="91145-160">輸出</span><span class="sxs-lookup"><span data-stu-id="91145-160">OUTPUTS</span></span>

### <span data-ttu-id="91145-161">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="91145-161">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="91145-162">筆記</span><span class="sxs-lookup"><span data-stu-id="91145-162">NOTES</span></span>

## <span data-ttu-id="91145-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="91145-163">RELATED LINKS</span></span>

[<span data-ttu-id="91145-164">AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="91145-164">Get-AzDeletedWebApp</span></span>](./Get-AzDeletedWebApp.md)