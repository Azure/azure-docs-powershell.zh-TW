---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplicationDefinition.md
ms.openlocfilehash: 947cd0674e5fcd704b305b5963f3ed06e008f3fe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906873"
---
# <span data-ttu-id="c2a06-101">New-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="c2a06-101">New-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="c2a06-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c2a06-102">SYNOPSIS</span></span>
<span data-ttu-id="c2a06-103">建立受管理的應用程式定義。</span><span class="sxs-lookup"><span data-stu-id="c2a06-103">Creates a managed application definition.</span></span>

## <span data-ttu-id="c2a06-104">語法</span><span class="sxs-lookup"><span data-stu-id="c2a06-104">SYNTAX</span></span>

```
New-AzManagedApplicationDefinition -Name <String> -ResourceGroupName <String> -DisplayName <String>
 -Description <String> -Location <String> -LockLevel <ApplicationLockLevel> [-PackageFileUri <String>]
 [-CreateUiDefinition <String>] [-MainTemplate <String>] -Authorization <String[]> [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c2a06-105">描述</span><span class="sxs-lookup"><span data-stu-id="c2a06-105">DESCRIPTION</span></span>
<span data-ttu-id="c2a06-106">**New-AzManagedApplicationDefinition** Cmdlet 會建立受管理的應用程式定義。</span><span class="sxs-lookup"><span data-stu-id="c2a06-106">The **New-AzManagedApplicationDefinition** cmdlet creates a managed application definition.</span></span>

## <span data-ttu-id="c2a06-107">例子</span><span class="sxs-lookup"><span data-stu-id="c2a06-107">EXAMPLES</span></span>

### <span data-ttu-id="c2a06-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="c2a06-108">Example 1</span></span>
```
PS> New-AzManagedApplicationDefinition -Name myAppDef -ResourceGroupName myRG -DisplayName test -Description "sample description" -Location westus -LockLevel ReadOnly -PackageFileUri https://sample.blob.core.windows.net/files/myPackage.zip -Authorization <principalId:roleDefinitionId>
```

<span data-ttu-id="c2a06-109">此命令會建立受管理的應用程式定義</span><span class="sxs-lookup"><span data-stu-id="c2a06-109">This command creates a managed application definition</span></span>

## <span data-ttu-id="c2a06-110">參數</span><span class="sxs-lookup"><span data-stu-id="c2a06-110">PARAMETERS</span></span>

### <span data-ttu-id="c2a06-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c2a06-111">-ApiVersion</span></span>
<span data-ttu-id="c2a06-112">設定時，表示要使用資源提供者 API 的版本。</span><span class="sxs-lookup"><span data-stu-id="c2a06-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="c2a06-113">如果未指定，API 版本會自動判斷為最新可用。</span><span class="sxs-lookup"><span data-stu-id="c2a06-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="c2a06-114">-授權</span><span class="sxs-lookup"><span data-stu-id="c2a06-114">-Authorization</span></span>
<span data-ttu-id="c2a06-115">受管理的應用程式定義授權。</span><span class="sxs-lookup"><span data-stu-id="c2a06-115">The managed application definition authorization.</span></span>
<span data-ttu-id="c2a06-116">逗號分隔授權組的格式為 \<principalId\> ：\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="c2a06-116">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2a06-117">-CreateUiDefinition</span><span class="sxs-lookup"><span data-stu-id="c2a06-117">-CreateUiDefinition</span></span>
<span data-ttu-id="c2a06-118">受管理的應用程式定義建立 ui 定義</span><span class="sxs-lookup"><span data-stu-id="c2a06-118">The managed application definition create ui definition</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2a06-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2a06-119">-DefaultProfile</span></span>
<span data-ttu-id="c2a06-120">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c2a06-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2a06-121">-描述</span><span class="sxs-lookup"><span data-stu-id="c2a06-121">-Description</span></span>
<span data-ttu-id="c2a06-122">受管理的應用程式定義描述。</span><span class="sxs-lookup"><span data-stu-id="c2a06-122">The managed application definition description.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2a06-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c2a06-123">-DisplayName</span></span>
<span data-ttu-id="c2a06-124">受管理的應用程式定義顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="c2a06-124">The managed application definition display name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2a06-125">-位置</span><span class="sxs-lookup"><span data-stu-id="c2a06-125">-Location</span></span>
<span data-ttu-id="c2a06-126">資源位置。</span><span class="sxs-lookup"><span data-stu-id="c2a06-126">The resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2a06-127">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="c2a06-127">-LockLevel</span></span>
<span data-ttu-id="c2a06-128">受管理應用程式定義的鎖定層級。</span><span class="sxs-lookup"><span data-stu-id="c2a06-128">The level of the lock for managed application definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationLockLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: None, CanNotDelete, ReadOnly

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2a06-129">-MainTemplate</span><span class="sxs-lookup"><span data-stu-id="c2a06-129">-MainTemplate</span></span>
<span data-ttu-id="c2a06-130">受管理的應用程式定義主範本</span><span class="sxs-lookup"><span data-stu-id="c2a06-130">The managed application definition main template</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2a06-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="c2a06-131">-Name</span></span>
<span data-ttu-id="c2a06-132">受管理的應用程式定義名稱。</span><span class="sxs-lookup"><span data-stu-id="c2a06-132">The managed application definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2a06-133">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="c2a06-133">-PackageFileUri</span></span>
<span data-ttu-id="c2a06-134">受管理的應用程式定義套件檔 uri。</span><span class="sxs-lookup"><span data-stu-id="c2a06-134">The managed application definition package file uri.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2a06-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="c2a06-135">-Pre</span></span>
<span data-ttu-id="c2a06-136">設定之後，表示當系統自動決定要使用哪個版本時，Cmdlet 應該使用測試版 API 版本。</span><span class="sxs-lookup"><span data-stu-id="c2a06-136">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="c2a06-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2a06-137">-ResourceGroupName</span></span>
<span data-ttu-id="c2a06-138">資源組名。</span><span class="sxs-lookup"><span data-stu-id="c2a06-138">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2a06-139">-標記</span><span class="sxs-lookup"><span data-stu-id="c2a06-139">-Tag</span></span>
<span data-ttu-id="c2a06-140">代表資源標記的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="c2a06-140">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2a06-141">-確認</span><span class="sxs-lookup"><span data-stu-id="c2a06-141">-Confirm</span></span>
<span data-ttu-id="c2a06-142">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c2a06-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2a06-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2a06-143">-WhatIf</span></span>
<span data-ttu-id="c2a06-144">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c2a06-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2a06-145">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c2a06-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2a06-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2a06-146">CommonParameters</span></span>
<span data-ttu-id="c2a06-147">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c2a06-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2a06-148">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c2a06-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2a06-149">輸入</span><span class="sxs-lookup"><span data-stu-id="c2a06-149">INPUTS</span></span>

### <span data-ttu-id="c2a06-150">System.String</span><span class="sxs-lookup"><span data-stu-id="c2a06-150">System.String</span></span>

### <span data-ttu-id="c2a06-151">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.application.ApplicationLockLevel</span><span class="sxs-lookup"><span data-stu-id="c2a06-151">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationLockLevel</span></span>

### <span data-ttu-id="c2a06-152">System.String[]</span><span class="sxs-lookup"><span data-stu-id="c2a06-152">System.String[]</span></span>

### <span data-ttu-id="c2a06-153">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="c2a06-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c2a06-154">輸出</span><span class="sxs-lookup"><span data-stu-id="c2a06-154">OUTPUTS</span></span>

### <span data-ttu-id="c2a06-155">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="c2a06-155">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="c2a06-156">筆記</span><span class="sxs-lookup"><span data-stu-id="c2a06-156">NOTES</span></span>

## <span data-ttu-id="c2a06-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="c2a06-157">RELATED LINKS</span></span>
