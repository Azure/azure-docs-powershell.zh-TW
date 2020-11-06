---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restore-azurermdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmDeletedWebApp.md
ms.openlocfilehash: caebbe3c9b84b469e5fc357686b256aca59c2b61
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449652"
---
# <span data-ttu-id="cf56b-101">Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="cf56b-101">Restore-AzureRmDeletedWebApp</span></span>

## <span data-ttu-id="cf56b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cf56b-102">SYNOPSIS</span></span>
<span data-ttu-id="cf56b-103">將已刪除的 web 應用程式還原到新的或現有的 web 應用程式。</span><span class="sxs-lookup"><span data-stu-id="cf56b-103">Restores a deleted web app to a new or existing web app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf56b-104">句法</span><span class="sxs-lookup"><span data-stu-id="cf56b-104">SYNTAX</span></span>

### <span data-ttu-id="cf56b-105">FromDeletedResourceName</span><span class="sxs-lookup"><span data-stu-id="cf56b-105">FromDeletedResourceName</span></span>
```
Restore-AzureRmDeletedWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf56b-106">FromDeletedApp</span><span class="sxs-lookup"><span data-stu-id="cf56b-106">FromDeletedApp</span></span>
```
Restore-AzureRmDeletedWebApp [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-InputObject] <PSAzureDeletedWebApp> [<CommonParameters>]
```

## <span data-ttu-id="cf56b-107">說明</span><span class="sxs-lookup"><span data-stu-id="cf56b-107">DESCRIPTION</span></span>
<span data-ttu-id="cf56b-108">**Restore-AzureRmDeletedWebApp** Cmdlet 會還原已刪除的 web 應用程式。</span><span class="sxs-lookup"><span data-stu-id="cf56b-108">The **Restore-AzureRmDeletedWebApp** cmdlet restores a deleted web app.</span></span> <span data-ttu-id="cf56b-109">TargetResourceGroupName、TargetName 和 TargetSlot 所指定的 web app 將會覆寫已刪除 web 應用程式的內容和設定。</span><span class="sxs-lookup"><span data-stu-id="cf56b-109">The web app specified by TargetResourceGroupName, TargetName, and TargetSlot will be overwritten with the contents and settings of the deleted web app.</span></span> <span data-ttu-id="cf56b-110">如果未指定目標參數，則會自動使用已刪除的 web 應用程式的資源群組、名稱和槽來填入它們。</span><span class="sxs-lookup"><span data-stu-id="cf56b-110">If the target parameters are not specified, they will automatically be filled with the deleted web app's resource group, name, and slot.</span></span> <span data-ttu-id="cf56b-111">如果目標 web 應用程式不存在，則會自動在 TargetAppServicePlanName 指定的 app 服務方案中建立它。</span><span class="sxs-lookup"><span data-stu-id="cf56b-111">If the target web app does not exist, it will automatically be created in the app service plan specified by TargetAppServicePlanName.</span></span> <span data-ttu-id="cf56b-112">RestoreContentOnly 切換參數只能用來還原已刪除 app 的檔案，而不需要 app 設定。</span><span class="sxs-lookup"><span data-stu-id="cf56b-112">The RestoreContentOnly switch parameter can be used to restore only the deleted app's files without the app settings.</span></span>

## <span data-ttu-id="cf56b-113">示例</span><span class="sxs-lookup"><span data-stu-id="cf56b-113">EXAMPLES</span></span>

### <span data-ttu-id="cf56b-114">範例1</span><span class="sxs-lookup"><span data-stu-id="cf56b-114">Example 1</span></span>
```powershell
PS C:\> Restore-AzureRmDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -TargetAppServicePlanName ContosoPlan
```

<span data-ttu-id="cf56b-115">還原名為 ContosoApp 的已刪除應用程式，其名稱為「資源群組預設-Web-WestUS」。</span><span class="sxs-lookup"><span data-stu-id="cf56b-115">Restores a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="cf56b-116">將會在名為 ContosoPlan 的應用程式服務方案中建立具有相同名稱和資源群組的新應用程式，並將已刪除的應用程式的檔案和設定還原到其中。</span><span class="sxs-lookup"><span data-stu-id="cf56b-116">A new app with the same name and resource group will be created in the App Service Plan named ContosoPlan, and the deleted app's files and settings will be restored to it.</span></span>

### <span data-ttu-id="cf56b-117">範例2</span><span class="sxs-lookup"><span data-stu-id="cf56b-117">Example 2</span></span>
```powershell
PS C:\> Restore-AzureRmDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -Slot Staging -TargetResourceGroupName Default-Web-EastUS -TargetName ContosoRestore -RestoreContentOnly
```

<span data-ttu-id="cf56b-118">還原名為 ContosoApp 的已刪除應用程式的暫存槽，其名稱為「資源群組預設-WestUS」。</span><span class="sxs-lookup"><span data-stu-id="cf56b-118">Restores the Staging slot of a deleted app named ContosoApp belonging to the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="cf56b-119">ContosoRestore 屬於資源群組的 web app （預設為 [網頁-EastUS]）將會被覆蓋。</span><span class="sxs-lookup"><span data-stu-id="cf56b-119">The web app named ContosoRestore belonging to the resource group Default-Web-EastUS will be overwritten.</span></span> <span data-ttu-id="cf56b-120">已刪除的 web 應用程式設定將無法還原。</span><span class="sxs-lookup"><span data-stu-id="cf56b-120">The deleted web app settings will not be restored.</span></span>

## <span data-ttu-id="cf56b-121">參數</span><span class="sxs-lookup"><span data-stu-id="cf56b-121">PARAMETERS</span></span>

### <span data-ttu-id="cf56b-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cf56b-122">-AsJob</span></span>
<span data-ttu-id="cf56b-123">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cf56b-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cf56b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf56b-124">-DefaultProfile</span></span>
<span data-ttu-id="cf56b-125">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cf56b-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf56b-126">-Force</span><span class="sxs-lookup"><span data-stu-id="cf56b-126">-Force</span></span>
<span data-ttu-id="cf56b-127">在不提示確認的情況下執行還原。</span><span class="sxs-lookup"><span data-stu-id="cf56b-127">Do the restore without prompting for confirmation.</span></span>

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

### <span data-ttu-id="cf56b-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf56b-128">-InputObject</span></span>
<span data-ttu-id="cf56b-129">已刪除的 Azure Web App。</span><span class="sxs-lookup"><span data-stu-id="cf56b-129">The deleted Azure Web App.</span></span>

```yaml
Type: PSAzureDeletedWebApp
Parameter Sets: FromDeletedApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf56b-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="cf56b-130">-Name</span></span>
<span data-ttu-id="cf56b-131">已刪除的 Azure Web 應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="cf56b-131">The name of the deleted Azure Web App.</span></span>

```yaml
Type: String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf56b-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf56b-132">-ResourceGroupName</span></span>
<span data-ttu-id="cf56b-133">已刪除的 Azure Web App 的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="cf56b-133">The resource group of the deleted Azure Web App.</span></span>

```yaml
Type: String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf56b-134">-RestoreContentOnly</span><span class="sxs-lookup"><span data-stu-id="cf56b-134">-RestoreContentOnly</span></span>
<span data-ttu-id="cf56b-135">還原 web 應用程式的檔案，但不要還原設定。</span><span class="sxs-lookup"><span data-stu-id="cf56b-135">Restore the web app's files, but do not restore the settings.</span></span>

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

### <span data-ttu-id="cf56b-136">-槽</span><span class="sxs-lookup"><span data-stu-id="cf56b-136">-Slot</span></span>
<span data-ttu-id="cf56b-137">已刪除的 Azure Web App 槽。</span><span class="sxs-lookup"><span data-stu-id="cf56b-137">The deleted Azure Web App slot.</span></span>

```yaml
Type: String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf56b-138">-TargetAppServicePlanName</span><span class="sxs-lookup"><span data-stu-id="cf56b-138">-TargetAppServicePlanName</span></span>
<span data-ttu-id="cf56b-139">新 Azure Web App 的 App 服務規劃。</span><span class="sxs-lookup"><span data-stu-id="cf56b-139">The App Service Plan for the new Azure Web App.</span></span>

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

### <span data-ttu-id="cf56b-140">-TargetName</span><span class="sxs-lookup"><span data-stu-id="cf56b-140">-TargetName</span></span>
<span data-ttu-id="cf56b-141">新的 Azure Web App 名稱。</span><span class="sxs-lookup"><span data-stu-id="cf56b-141">The name of the new Azure Web App.</span></span>

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

### <span data-ttu-id="cf56b-142">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf56b-142">-TargetResourceGroupName</span></span>
<span data-ttu-id="cf56b-143">包含新 Azure Web App 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="cf56b-143">The resource group containing the new Azure Web App.</span></span>

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

### <span data-ttu-id="cf56b-144">-TargetSlot</span><span class="sxs-lookup"><span data-stu-id="cf56b-144">-TargetSlot</span></span>
<span data-ttu-id="cf56b-145">新的 Azure Web App 槽的名稱。</span><span class="sxs-lookup"><span data-stu-id="cf56b-145">The name of the new Azure Web App slot.</span></span>

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

### <span data-ttu-id="cf56b-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf56b-146">CommonParameters</span></span>
<span data-ttu-id="cf56b-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cf56b-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="cf56b-148">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cf56b-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf56b-149">輸入</span><span class="sxs-lookup"><span data-stu-id="cf56b-149">INPUTS</span></span>

### <span data-ttu-id="cf56b-150">WebApps WebApps. PSAzureDeletedWebApp （）</span><span class="sxs-lookup"><span data-stu-id="cf56b-150">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="cf56b-151">輸出</span><span class="sxs-lookup"><span data-stu-id="cf56b-151">OUTPUTS</span></span>

### <span data-ttu-id="cf56b-152">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="cf56b-152">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="cf56b-153">筆記</span><span class="sxs-lookup"><span data-stu-id="cf56b-153">NOTES</span></span>

## <span data-ttu-id="cf56b-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="cf56b-154">RELATED LINKS</span></span>

[<span data-ttu-id="cf56b-155">AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="cf56b-155">Get-AzureRmDeletedWebApp</span></span>](./Get-AzureRmDeletedWebApp.md)
