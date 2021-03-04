---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/restore-azdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzDeletedWebApp.md
ms.openlocfilehash: 81807c92b336bd171d0890f5b3e948ec11313023
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914970"
---
# <span data-ttu-id="1dbe0-101">Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="1dbe0-101">Restore-AzDeletedWebApp</span></span>

## <span data-ttu-id="1dbe0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1dbe0-102">SYNOPSIS</span></span>
<span data-ttu-id="1dbe0-103">將已刪除的 Web App 還原至新的或現有的 Web App。</span><span class="sxs-lookup"><span data-stu-id="1dbe0-103">Restores a deleted web app to a new or existing web app.</span></span>

## <span data-ttu-id="1dbe0-104">語法</span><span class="sxs-lookup"><span data-stu-id="1dbe0-104">SYNTAX</span></span>

### <span data-ttu-id="1dbe0-105">FromDeletedResourceName (預設) </span><span class="sxs-lookup"><span data-stu-id="1dbe0-105">FromDeletedResourceName (Default)</span></span>
```
Restore-AzDeletedWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-Location <String>]
 [-DeletedId <String>] [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-UseDisasterRecovery] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dbe0-106">FromDeletedApp</span><span class="sxs-lookup"><span data-stu-id="1dbe0-106">FromDeletedApp</span></span>
```
Restore-AzDeletedWebApp [-TargetResourceGroupName <String>] [-DeletedId <String>] [-TargetName <String>] 
 [-TargetSlot <String>] [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-UseDisasterRecovery] 
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-InputObject] <PSAzureDeletedWebApp> 
 [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1dbe0-107">描述</span><span class="sxs-lookup"><span data-stu-id="1dbe0-107">DESCRIPTION</span></span>
<span data-ttu-id="1dbe0-108">**Restore-AzDeletedWebApp** Cmdlet 會還原已刪除的 Web App。</span><span class="sxs-lookup"><span data-stu-id="1dbe0-108">The **Restore-AzDeletedWebApp** cmdlet restores a deleted web app.</span></span> <span data-ttu-id="1dbe0-109">TargetResourceGroupName、TargetName 和 TargetSlot 指定的 Web 應用程式會以已刪除之 Web App 的內容和設定來覆蓋。</span><span class="sxs-lookup"><span data-stu-id="1dbe0-109">The web app specified by TargetResourceGroupName, TargetName, and TargetSlot will be overwritten with the contents and settings of the deleted web app.</span></span> <span data-ttu-id="1dbe0-110">如果未指定目標參數，系統會自動填入已刪除之 Web App 的資源群組、名稱和時段。</span><span class="sxs-lookup"><span data-stu-id="1dbe0-110">If the target parameters are not specified, they will automatically be filled with the deleted web app's resource group, name, and slot.</span></span> <span data-ttu-id="1dbe0-111">如果目標 Web App 不存在，它會自動在 TargetAppServicePlanName 指定的應用程式服務計畫中建立。</span><span class="sxs-lookup"><span data-stu-id="1dbe0-111">If the target web app does not exist, it will automatically be created in the app service plan specified by TargetAppServicePlanName.</span></span> <span data-ttu-id="1dbe0-112">RestoreContentOnly 參數只能用來還原已刪除的 App 檔案，而不需要應用程式設定。</span><span class="sxs-lookup"><span data-stu-id="1dbe0-112">The RestoreContentOnly switch parameter can be used to restore only the deleted app's files without the app settings.</span></span>

## <span data-ttu-id="1dbe0-113">例子</span><span class="sxs-lookup"><span data-stu-id="1dbe0-113">EXAMPLES</span></span>

### <span data-ttu-id="1dbe0-114">範例 1</span><span class="sxs-lookup"><span data-stu-id="1dbe0-114">Example 1</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -TargetAppServicePlanName ContosoPlan
```

<span data-ttu-id="1dbe0-115">還原名稱為 ContosoApp 的已刪除應用程式，該應用程式屬於資源群組 Default-Web-WestUS。</span><span class="sxs-lookup"><span data-stu-id="1dbe0-115">Restores a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="1dbe0-116">在名為 ContosoPlan 的應用程式服務計畫中，將會建立一個名稱與資源群組相同的新應用程式，而已刪除的應用程式檔案和設定將會還原至該應用程式。</span><span class="sxs-lookup"><span data-stu-id="1dbe0-116">A new app with the same name and resource group will be created in the App Service Plan named ContosoPlan, and the deleted app's files and settings will be restored to it.</span></span>

### <span data-ttu-id="1dbe0-117">範例 2</span><span class="sxs-lookup"><span data-stu-id="1dbe0-117">Example 2</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -Slot Staging -TargetResourceGroupName Default-Web-EastUS -TargetName ContosoRestore -RestoreContentOnly
```

<span data-ttu-id="1dbe0-118">還原屬於資源群組 Default-Web-WestUS 的已刪除應用程式 ContosoApp 的暫存時段。</span><span class="sxs-lookup"><span data-stu-id="1dbe0-118">Restores the Staging slot of a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="1dbe0-119">名稱為 ContosoRestore 的 Web 應用程式屬於資源群組 Default-Web-EastUS，將會受到覆蓋。</span><span class="sxs-lookup"><span data-stu-id="1dbe0-119">The web app named ContosoRestore belonging to the resource group Default-Web-EastUS will be overwritten.</span></span> <span data-ttu-id="1dbe0-120">已刪除的 Web App 設定將不會還原。</span><span class="sxs-lookup"><span data-stu-id="1dbe0-120">The deleted web app settings will not be restored.</span></span>

###<span data-ttu-id="1dbe0-121">範例 3</span><span class="sxs-lookup"><span data-stu-id="1dbe0-121">Example 3</span></span>
```powershell
PS C:\> Restore-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -DeletedId /subscriptions/00000000-0000-0000-0000-000000000000/providers/Microsoft.Web/locations/location/deletedSites/1234 -TargetAppServicePlanName ContosoPlan
```

<span data-ttu-id="1dbe0-122">如果有 2 個已刪除且名稱相同的應用程式 (ContosoApp) ，我們會同時取得網站詳細資料，並撥打 Id 還原，以我們所選擇的應用程式還原名為 ContosoRestore 的應用程式。</span><span class="sxs-lookup"><span data-stu-id="1dbe0-122">In case there are 2 deleted apps with same name(ContosoApp), then we get details of both the sites and restore the app named ContosoRestore with the app of our choice by calling restore with Id.</span></span>

###<span data-ttu-id="1dbe0-123">範例 4</span><span class="sxs-lookup"><span data-stu-id="1dbe0-123">Example 4</span></span>
```powershell
PS C:\> $deletedSite = Get-AzDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp
PS C:\> Restore-AzDeletedWebApp -TargetResourceGroupName Default-Web-EastUS -TargetName ContosoRestore -TargetAppServicePlanName ContosoPlan -InputObject $deletedSite[0]
```

<span data-ttu-id="1dbe0-124">如果有 2 個已刪除且名稱相同的應用程式 (ContosoApp) ，我們會同時取得網站詳細資料，並撥打 InputObject (Deletedsite) 來使用我們所選擇的應用程式還原名為 ContosoRestore 的應用程式</span><span class="sxs-lookup"><span data-stu-id="1dbe0-124">In case there are 2 deleted apps with same name(ContosoApp), then we get details of both the sites and restore the app named ContosoRestore with the app of our choice by calling restore with InputObject(Deletedsite) details</span></span> 

## <span data-ttu-id="1dbe0-125">參數</span><span class="sxs-lookup"><span data-stu-id="1dbe0-125">PARAMETERS</span></span>

### <span data-ttu-id="1dbe0-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1dbe0-126">-AsJob</span></span>
<span data-ttu-id="1dbe0-127">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1dbe0-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1dbe0-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dbe0-128">-DefaultProfile</span></span>
<span data-ttu-id="1dbe0-129">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1dbe0-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1dbe0-130">-DeletedId</span><span class="sxs-lookup"><span data-stu-id="1dbe0-130">-DeletedId</span></span>
<span data-ttu-id="1dbe0-131">已刪除的 Azure Web App 識別碼。</span><span class="sxs-lookup"><span data-stu-id="1dbe0-131">The Id of the deleted Azure Web App.</span></span>

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

### <span data-ttu-id="1dbe0-132">-強制</span><span class="sxs-lookup"><span data-stu-id="1dbe0-132">-Force</span></span>
<span data-ttu-id="1dbe0-133">執行還原，但不提示確認。</span><span class="sxs-lookup"><span data-stu-id="1dbe0-133">Do the restore without prompting for confirmation.</span></span>

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

### <span data-ttu-id="1dbe0-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1dbe0-134">-InputObject</span></span>
<span data-ttu-id="1dbe0-135">已刪除的 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="1dbe0-135">The deleted Azure Web App.</span></span>

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

### <span data-ttu-id="1dbe0-136">-位置</span><span class="sxs-lookup"><span data-stu-id="1dbe0-136">-Location</span></span>
<span data-ttu-id="1dbe0-137">已刪除的 Azure Web App 位置。</span><span class="sxs-lookup"><span data-stu-id="1dbe0-137">The location of the deleted Azure Web App.</span></span>

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

### <span data-ttu-id="1dbe0-138">-名稱</span><span class="sxs-lookup"><span data-stu-id="1dbe0-138">-Name</span></span>
<span data-ttu-id="1dbe0-139">已刪除的 Azure Web App 名稱。</span><span class="sxs-lookup"><span data-stu-id="1dbe0-139">The name of the deleted Azure Web App.</span></span>

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

### <span data-ttu-id="1dbe0-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dbe0-140">-ResourceGroupName</span></span>
<span data-ttu-id="1dbe0-141">已刪除的 Azure Web App 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="1dbe0-141">The resource group of the deleted Azure Web App.</span></span>

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

### <span data-ttu-id="1dbe0-142">-RestoreContentOnly</span><span class="sxs-lookup"><span data-stu-id="1dbe0-142">-RestoreContentOnly</span></span>
<span data-ttu-id="1dbe0-143">還原 Web App 的檔案，但不還原設定。</span><span class="sxs-lookup"><span data-stu-id="1dbe0-143">Restore the web app's files, but do not restore the settings.</span></span>

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

### <span data-ttu-id="1dbe0-144">-Slot</span><span class="sxs-lookup"><span data-stu-id="1dbe0-144">-Slot</span></span>
<span data-ttu-id="1dbe0-145">已刪除的 Azure Web App 插槽。</span><span class="sxs-lookup"><span data-stu-id="1dbe0-145">The deleted Azure Web App slot.</span></span>

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

### <span data-ttu-id="1dbe0-146">-TargetAppServicePlanName</span><span class="sxs-lookup"><span data-stu-id="1dbe0-146">-TargetAppServicePlanName</span></span>
<span data-ttu-id="1dbe0-147">適用于新 Azure Web App 的應用程式服務方案。</span><span class="sxs-lookup"><span data-stu-id="1dbe0-147">The App Service Plan for the new Azure Web App.</span></span>

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

### <span data-ttu-id="1dbe0-148">-TargetName</span><span class="sxs-lookup"><span data-stu-id="1dbe0-148">-TargetName</span></span>
<span data-ttu-id="1dbe0-149">新 Azure Web App 的名稱。</span><span class="sxs-lookup"><span data-stu-id="1dbe0-149">The name of the new Azure Web App.</span></span>

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

### <span data-ttu-id="1dbe0-150">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dbe0-150">-TargetResourceGroupName</span></span>
<span data-ttu-id="1dbe0-151">包含新 Azure Web App 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="1dbe0-151">The resource group containing the new Azure Web App.</span></span>

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

### <span data-ttu-id="1dbe0-152">-TargetSlot</span><span class="sxs-lookup"><span data-stu-id="1dbe0-152">-TargetSlot</span></span>
<span data-ttu-id="1dbe0-153">新 Azure Web App 插槽的名稱。</span><span class="sxs-lookup"><span data-stu-id="1dbe0-153">The name of the new Azure Web App slot.</span></span>

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

### <span data-ttu-id="1dbe0-154">-UseD區sterRecovery</span><span class="sxs-lookup"><span data-stu-id="1dbe0-154">-UseDisasterRecovery</span></span>
<span data-ttu-id="1dbe0-155">用於從離線的縮放單位復原已刪除的應用程式。</span><span class="sxs-lookup"><span data-stu-id="1dbe0-155">Use to recover a deleted app from a scale unit that is offline.</span></span>

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

### <span data-ttu-id="1dbe0-156">-確認</span><span class="sxs-lookup"><span data-stu-id="1dbe0-156">-Confirm</span></span>
<span data-ttu-id="1dbe0-157">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="1dbe0-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dbe0-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dbe0-158">-WhatIf</span></span>
<span data-ttu-id="1dbe0-159">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1dbe0-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1dbe0-160">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1dbe0-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1dbe0-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dbe0-161">CommonParameters</span></span>
<span data-ttu-id="1dbe0-162">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1dbe0-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dbe0-163">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="1dbe0-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dbe0-164">輸入</span><span class="sxs-lookup"><span data-stu-id="1dbe0-164">INPUTS</span></span>

### <span data-ttu-id="1dbe0-165">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="1dbe0-165">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="1dbe0-166">輸出</span><span class="sxs-lookup"><span data-stu-id="1dbe0-166">OUTPUTS</span></span>

### <span data-ttu-id="1dbe0-167">Microsoft.Azure.Commands.WebApps.models.PSSite</span><span class="sxs-lookup"><span data-stu-id="1dbe0-167">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="1dbe0-168">筆記</span><span class="sxs-lookup"><span data-stu-id="1dbe0-168">NOTES</span></span>

## <span data-ttu-id="1dbe0-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="1dbe0-169">RELATED LINKS</span></span>

[<span data-ttu-id="1dbe0-170">Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="1dbe0-170">Get-AzDeletedWebApp</span></span>](./Get-AzDeletedWebApp.md)