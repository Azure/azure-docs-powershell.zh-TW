---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restore-azwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzWebAppSnapshot.md
ms.openlocfilehash: 1dd84305753edc8ad639c160c9003c4c393d041e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128379"
---
# <span data-ttu-id="a8ee4-101">Restore-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="a8ee4-101">Restore-AzWebAppSnapshot</span></span>

## <span data-ttu-id="a8ee4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a8ee4-102">SYNOPSIS</span></span>
<span data-ttu-id="a8ee4-103">還原 web 應用程式快照。</span><span class="sxs-lookup"><span data-stu-id="a8ee4-103">Restores a web app snapshot.</span></span>

## <span data-ttu-id="a8ee4-104">句法</span><span class="sxs-lookup"><span data-stu-id="a8ee4-104">SYNTAX</span></span>

### <span data-ttu-id="a8ee4-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="a8ee4-105">FromResourceName</span></span>
```
Restore-AzWebAppSnapshot [-RecoverConfiguration] [-UseDisasterRecovery] [-Force] [-AsJob]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8ee4-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="a8ee4-106">FromWebApp</span></span>
```
Restore-AzWebAppSnapshot [-RecoverConfiguration] [-UseDisasterRecovery] [-Force] [-AsJob] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a8ee4-107">說明</span><span class="sxs-lookup"><span data-stu-id="a8ee4-107">DESCRIPTION</span></span>
<span data-ttu-id="a8ee4-108">將 web 應用程式快照還原至 web 應用程式。</span><span class="sxs-lookup"><span data-stu-id="a8ee4-108">Restores a web app snapshot to the web app.</span></span> <span data-ttu-id="a8ee4-109">還原快照時，會使用快照中包含的檔案，覆寫 web app 中的所有檔案。</span><span class="sxs-lookup"><span data-stu-id="a8ee4-109">Restoring a snapshot overwrites all files in a web app with the files contained in the snapshot.</span></span> <span data-ttu-id="a8ee4-110">若要同時還原設定，請使用 RecoverConfiguration 切換參數。</span><span class="sxs-lookup"><span data-stu-id="a8ee4-110">To restore settings as well, use the RecoverConfiguration switch parameter.</span></span> <span data-ttu-id="a8ee4-111">您可以將來自單一 web 應用程式的快照還原至相同訂閱中的任何其他 web 應用程式。</span><span class="sxs-lookup"><span data-stu-id="a8ee4-111">A snapshot from one web app can be restored to any other web app in the same subscription.</span></span>

## <span data-ttu-id="a8ee4-112">示例</span><span class="sxs-lookup"><span data-stu-id="a8ee4-112">EXAMPLES</span></span>

### <span data-ttu-id="a8ee4-113">範例1</span><span class="sxs-lookup"><span data-stu-id="a8ee4-113">Example 1</span></span>
```
PS C:\> $snapshot = (Get-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging")[0]
PS C:\> Restore-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Restore" -InputObject $snapshot -RecoverConfiguration
```

<span data-ttu-id="a8ee4-114">取得名為「ContosoApp」的 web 應用程式的最新快照，其中包含「Default-Web-WestUS」資源群組中名為「暫存」的槽。</span><span class="sxs-lookup"><span data-stu-id="a8ee4-114">Gets the latest snapshot of a web app named "ContosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group.</span></span> <span data-ttu-id="a8ee4-115">將快照還原至 web 應用程式的「還原」槽。</span><span class="sxs-lookup"><span data-stu-id="a8ee4-115">Restores the snapshot to the web app's "Restore" slot.</span></span>

## <span data-ttu-id="a8ee4-116">參數</span><span class="sxs-lookup"><span data-stu-id="a8ee4-116">PARAMETERS</span></span>

### <span data-ttu-id="a8ee4-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a8ee4-117">-AsJob</span></span>
<span data-ttu-id="a8ee4-118">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a8ee4-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a8ee4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8ee4-119">-DefaultProfile</span></span>
<span data-ttu-id="a8ee4-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a8ee4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8ee4-121">-Force</span><span class="sxs-lookup"><span data-stu-id="a8ee4-121">-Force</span></span>
<span data-ttu-id="a8ee4-122">允許覆蓋原始的 web 應用程式，而不顯示警告。</span><span class="sxs-lookup"><span data-stu-id="a8ee4-122">Allows the original web app to be overwritten without displaying a warning.</span></span>

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

### <span data-ttu-id="a8ee4-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a8ee4-123">-InputObject</span></span>
<span data-ttu-id="a8ee4-124">Azure Web App 快照。</span><span class="sxs-lookup"><span data-stu-id="a8ee4-124">The Azure Web App snapshot.</span></span>

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

### <span data-ttu-id="a8ee4-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="a8ee4-125">-Name</span></span>
<span data-ttu-id="a8ee4-126">Web 應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="a8ee4-126">The name of the web app.</span></span>

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

### <span data-ttu-id="a8ee4-127">-RecoverConfiguration</span><span class="sxs-lookup"><span data-stu-id="a8ee4-127">-RecoverConfiguration</span></span>
<span data-ttu-id="a8ee4-128">除了檔案之外，還能復原 web 應用程式的配置。</span><span class="sxs-lookup"><span data-stu-id="a8ee4-128">Recover the web app's configuration in addition to files.</span></span>

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

### <span data-ttu-id="a8ee4-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8ee4-129">-ResourceGroupName</span></span>
<span data-ttu-id="a8ee4-130">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a8ee4-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="a8ee4-131">-槽</span><span class="sxs-lookup"><span data-stu-id="a8ee4-131">-Slot</span></span>
<span data-ttu-id="a8ee4-132">Web 應用程式槽的名稱。</span><span class="sxs-lookup"><span data-stu-id="a8ee4-132">The name of the web app slot.</span></span>

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

### <span data-ttu-id="a8ee4-133">-UseDisasterRecovery</span><span class="sxs-lookup"><span data-stu-id="a8ee4-133">-UseDisasterRecovery</span></span>
<span data-ttu-id="a8ee4-134">用來從離線的縮放單位復原快照。</span><span class="sxs-lookup"><span data-stu-id="a8ee4-134">Use to recover a snapshot from a scale unit that is offline.</span></span>

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

### <span data-ttu-id="a8ee4-135">-WebApp</span><span class="sxs-lookup"><span data-stu-id="a8ee4-135">-WebApp</span></span>
<span data-ttu-id="a8ee4-136">Web app 物件</span><span class="sxs-lookup"><span data-stu-id="a8ee4-136">The web app object</span></span>

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

### <span data-ttu-id="a8ee4-137">-確認</span><span class="sxs-lookup"><span data-stu-id="a8ee4-137">-Confirm</span></span>
<span data-ttu-id="a8ee4-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a8ee4-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8ee4-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8ee4-139">-WhatIf</span></span>
<span data-ttu-id="a8ee4-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a8ee4-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8ee4-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a8ee4-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8ee4-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8ee4-142">CommonParameters</span></span>
<span data-ttu-id="a8ee4-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a8ee4-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8ee4-144">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a8ee4-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8ee4-145">輸入</span><span class="sxs-lookup"><span data-stu-id="a8ee4-145">INPUTS</span></span>

### <span data-ttu-id="a8ee4-146">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="a8ee4-146">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="a8ee4-147">System.object</span><span class="sxs-lookup"><span data-stu-id="a8ee4-147">System.String</span></span>

### <span data-ttu-id="a8ee4-148">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="a8ee4-148">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

### <span data-ttu-id="a8ee4-149">WebApps BackupRestore. AzureWebAppSnapshot （）</span><span class="sxs-lookup"><span data-stu-id="a8ee4-149">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>

## <span data-ttu-id="a8ee4-150">輸出</span><span class="sxs-lookup"><span data-stu-id="a8ee4-150">OUTPUTS</span></span>

### <span data-ttu-id="a8ee4-151">System.void</span><span class="sxs-lookup"><span data-stu-id="a8ee4-151">System.Void</span></span>

## <span data-ttu-id="a8ee4-152">筆記</span><span class="sxs-lookup"><span data-stu-id="a8ee4-152">NOTES</span></span>

## <span data-ttu-id="a8ee4-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="a8ee4-153">RELATED LINKS</span></span>