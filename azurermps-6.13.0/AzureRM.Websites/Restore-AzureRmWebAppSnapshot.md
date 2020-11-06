---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restore-azurermwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmWebAppSnapshot.md
ms.openlocfilehash: 536d0fe0f32231bfd732698c584e02be95d5c20e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448147"
---
# <span data-ttu-id="4bc49-101">Restore-AzureRmWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="4bc49-101">Restore-AzureRmWebAppSnapshot</span></span>

## <span data-ttu-id="4bc49-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4bc49-102">SYNOPSIS</span></span>
<span data-ttu-id="4bc49-103">還原 web 應用程式快照。</span><span class="sxs-lookup"><span data-stu-id="4bc49-103">Restores a web app snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4bc49-104">句法</span><span class="sxs-lookup"><span data-stu-id="4bc49-104">SYNTAX</span></span>

### <span data-ttu-id="4bc49-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="4bc49-105">FromResourceName</span></span>
```
Restore-AzureRmWebAppSnapshot [-RecoverConfiguration] [-Force] [-AsJob] [-ResourceGroupName] <String>
 [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4bc49-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="4bc49-106">FromWebApp</span></span>
```
Restore-AzureRmWebAppSnapshot [-RecoverConfiguration] [-Force] [-AsJob] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4bc49-107">說明</span><span class="sxs-lookup"><span data-stu-id="4bc49-107">DESCRIPTION</span></span>
<span data-ttu-id="4bc49-108">將 web 應用程式快照還原至 web 應用程式。</span><span class="sxs-lookup"><span data-stu-id="4bc49-108">Restores a web app snapshot to the web app.</span></span> <span data-ttu-id="4bc49-109">還原快照時，會使用快照中包含的檔案，覆寫 web app 中的所有檔案。</span><span class="sxs-lookup"><span data-stu-id="4bc49-109">Restoring a snapshot overwrites all files in a web app with the files contained in the snapshot.</span></span> <span data-ttu-id="4bc49-110">若要同時還原設定，請使用 RecoverConfiguration 切換參數。</span><span class="sxs-lookup"><span data-stu-id="4bc49-110">To restore settings as well, use the RecoverConfiguration switch parameter.</span></span> <span data-ttu-id="4bc49-111">您可以將來自單一 web 應用程式的快照還原至相同訂閱中的任何其他 web 應用程式。</span><span class="sxs-lookup"><span data-stu-id="4bc49-111">A snapshot from one web app can be restored to any other web app in the same subscription.</span></span>

## <span data-ttu-id="4bc49-112">示例</span><span class="sxs-lookup"><span data-stu-id="4bc49-112">EXAMPLES</span></span>

### <span data-ttu-id="4bc49-113">範例1</span><span class="sxs-lookup"><span data-stu-id="4bc49-113">Example 1</span></span>
```
PS C:\> $snapshot = (Get-AzureRmWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging")[0]
PS C:\> Restore-AzureRmWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Restore" -InputObject $snapshot -RecoverConfiguration
```

<span data-ttu-id="4bc49-114">取得名為「ContosoApp」的 web 應用程式的最新快照，其中包含「Default-Web-WestUS」資源群組中名為「暫存」的槽。</span><span class="sxs-lookup"><span data-stu-id="4bc49-114">Gets the latest snapshot of a web app named "ContosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group.</span></span> <span data-ttu-id="4bc49-115">將快照還原至 web 應用程式的「還原」槽。</span><span class="sxs-lookup"><span data-stu-id="4bc49-115">Restores the snapshot to the web app's "Restore" slot.</span></span>

## <span data-ttu-id="4bc49-116">參數</span><span class="sxs-lookup"><span data-stu-id="4bc49-116">PARAMETERS</span></span>

### <span data-ttu-id="4bc49-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4bc49-117">-AsJob</span></span>
<span data-ttu-id="4bc49-118">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="4bc49-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4bc49-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bc49-119">-DefaultProfile</span></span>
<span data-ttu-id="4bc49-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4bc49-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bc49-121">-Force</span><span class="sxs-lookup"><span data-stu-id="4bc49-121">-Force</span></span>
<span data-ttu-id="4bc49-122">允許覆蓋原始的 web 應用程式，而不顯示警告。</span><span class="sxs-lookup"><span data-stu-id="4bc49-122">Allows the original web app to be overwritten without displaying a warning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bc49-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4bc49-123">-InputObject</span></span>
<span data-ttu-id="4bc49-124">Azure Web App 快照。</span><span class="sxs-lookup"><span data-stu-id="4bc49-124">The Azure Web App snapshot.</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4bc49-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="4bc49-125">-Name</span></span>
<span data-ttu-id="4bc49-126">Web 應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="4bc49-126">The name of the web app.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bc49-127">-RecoverConfiguration</span><span class="sxs-lookup"><span data-stu-id="4bc49-127">-RecoverConfiguration</span></span>
<span data-ttu-id="4bc49-128">除了檔案之外，還能復原 web 應用程式的配置。</span><span class="sxs-lookup"><span data-stu-id="4bc49-128">Recover the web app's configuration in addition to files.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bc49-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bc49-129">-ResourceGroupName</span></span>
<span data-ttu-id="4bc49-130">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4bc49-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bc49-131">-槽</span><span class="sxs-lookup"><span data-stu-id="4bc49-131">-Slot</span></span>
<span data-ttu-id="4bc49-132">Web 應用程式槽的名稱。</span><span class="sxs-lookup"><span data-stu-id="4bc49-132">The name of the web app slot.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bc49-133">-WebApp</span><span class="sxs-lookup"><span data-stu-id="4bc49-133">-WebApp</span></span>
<span data-ttu-id="4bc49-134">Web app 物件</span><span class="sxs-lookup"><span data-stu-id="4bc49-134">The web app object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: FromWebApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4bc49-135">-確認</span><span class="sxs-lookup"><span data-stu-id="4bc49-135">-Confirm</span></span>
<span data-ttu-id="4bc49-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4bc49-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4bc49-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bc49-137">-WhatIf</span></span>
<span data-ttu-id="4bc49-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4bc49-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4bc49-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4bc49-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4bc49-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bc49-140">CommonParameters</span></span>
<span data-ttu-id="4bc49-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4bc49-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bc49-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4bc49-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bc49-143">輸入</span><span class="sxs-lookup"><span data-stu-id="4bc49-143">INPUTS</span></span>

### <span data-ttu-id="4bc49-144">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="4bc49-144">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="4bc49-145">System.object</span><span class="sxs-lookup"><span data-stu-id="4bc49-145">System.String</span></span>

### <span data-ttu-id="4bc49-146">[Microsoft Azure. 管理] 網站</span><span class="sxs-lookup"><span data-stu-id="4bc49-146">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="4bc49-147">參數： WebApp (ByValue) </span><span class="sxs-lookup"><span data-stu-id="4bc49-147">Parameters: WebApp (ByValue)</span></span>

### <span data-ttu-id="4bc49-148">WebApps BackupRestore. AzureWebAppSnapshot （）</span><span class="sxs-lookup"><span data-stu-id="4bc49-148">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>
<span data-ttu-id="4bc49-149">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="4bc49-149">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="4bc49-150">輸出</span><span class="sxs-lookup"><span data-stu-id="4bc49-150">OUTPUTS</span></span>

### <span data-ttu-id="4bc49-151">System.void</span><span class="sxs-lookup"><span data-stu-id="4bc49-151">System.Void</span></span>

## <span data-ttu-id="4bc49-152">筆記</span><span class="sxs-lookup"><span data-stu-id="4bc49-152">NOTES</span></span>

## <span data-ttu-id="4bc49-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="4bc49-153">RELATED LINKS</span></span>
