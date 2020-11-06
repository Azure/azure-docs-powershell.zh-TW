---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmManagedApplicationDefinition.md
ms.openlocfilehash: ebabe915fd203ffd73c111b0be5a2e82e2bea3a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93443704"
---
# <span data-ttu-id="513b5-101">New-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="513b5-101">New-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="513b5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="513b5-102">SYNOPSIS</span></span>
<span data-ttu-id="513b5-103">建立受管理的應用程式定義。</span><span class="sxs-lookup"><span data-stu-id="513b5-103">Creates a managed application definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="513b5-104">句法</span><span class="sxs-lookup"><span data-stu-id="513b5-104">SYNTAX</span></span>

```
New-AzureRmManagedApplicationDefinition -Name <String> -ResourceGroupName <String> -DisplayName <String>
 -Description <String> -Location <String> -LockLevel <ApplicationLockLevel> [-PackageFileUri <String>]
 [-CreateUiDefinition <String>] [-MainTemplate <String>] -Authorization <String[]> [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="513b5-105">說明</span><span class="sxs-lookup"><span data-stu-id="513b5-105">DESCRIPTION</span></span>
<span data-ttu-id="513b5-106">**新的-AzureRmManagedApplicationDefinition** Cmdlet 會建立受管理的應用程式定義。</span><span class="sxs-lookup"><span data-stu-id="513b5-106">The **New-AzureRmManagedApplicationDefinition** cmdlet creates a managed application definition.</span></span>

## <span data-ttu-id="513b5-107">示例</span><span class="sxs-lookup"><span data-stu-id="513b5-107">EXAMPLES</span></span>

### <span data-ttu-id="513b5-108">範例1</span><span class="sxs-lookup"><span data-stu-id="513b5-108">Example 1</span></span>
```
PS> New-AzureRmManagedApplicationDefinition -Name myAppDef -ResourceGroupName myRG -DisplayName test -Description "sample description" -Location westus -LockLevel ReadOnly -PackageFileUri https://sample.blob.core.windows.net/files/myPackage.zip -Authorization <principalId:roleDefinitionId>
```

<span data-ttu-id="513b5-109">這個命令會建立受管理的應用程式定義</span><span class="sxs-lookup"><span data-stu-id="513b5-109">This command creates a managed application definition</span></span>

## <span data-ttu-id="513b5-110">參數</span><span class="sxs-lookup"><span data-stu-id="513b5-110">PARAMETERS</span></span>

### <span data-ttu-id="513b5-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="513b5-111">-ApiVersion</span></span>
<span data-ttu-id="513b5-112">設定時，會指出要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="513b5-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="513b5-113">如果未指定，API 版本會自動決定為最新的可用。</span><span class="sxs-lookup"><span data-stu-id="513b5-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="513b5-114">-授權</span><span class="sxs-lookup"><span data-stu-id="513b5-114">-Authorization</span></span>
<span data-ttu-id="513b5-115">受管理的應用程式定義授權。</span><span class="sxs-lookup"><span data-stu-id="513b5-115">The managed application definition authorization.</span></span>
<span data-ttu-id="513b5-116">以逗號分隔授權對的格式 \<principalId\> ：\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="513b5-116">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

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

### <span data-ttu-id="513b5-117">-CreateUiDefinition</span><span class="sxs-lookup"><span data-stu-id="513b5-117">-CreateUiDefinition</span></span>
<span data-ttu-id="513b5-118">受管理的應用程式定義建立使用者介面定義</span><span class="sxs-lookup"><span data-stu-id="513b5-118">The managed application definition create ui definition</span></span>

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

### <span data-ttu-id="513b5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="513b5-119">-DefaultProfile</span></span>
<span data-ttu-id="513b5-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="513b5-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="513b5-121">-描述</span><span class="sxs-lookup"><span data-stu-id="513b5-121">-Description</span></span>
<span data-ttu-id="513b5-122">受管理的應用程式定義說明。</span><span class="sxs-lookup"><span data-stu-id="513b5-122">The managed application definition description.</span></span>

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

### <span data-ttu-id="513b5-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="513b5-123">-DisplayName</span></span>
<span data-ttu-id="513b5-124">受管理的應用程式定義顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="513b5-124">The managed application definition display name.</span></span>

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

### <span data-ttu-id="513b5-125">-位置</span><span class="sxs-lookup"><span data-stu-id="513b5-125">-Location</span></span>
<span data-ttu-id="513b5-126">資源位置。</span><span class="sxs-lookup"><span data-stu-id="513b5-126">The resource location.</span></span>

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

### <span data-ttu-id="513b5-127">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="513b5-127">-LockLevel</span></span>
<span data-ttu-id="513b5-128">受管理的應用程式定義鎖定的層級。</span><span class="sxs-lookup"><span data-stu-id="513b5-128">The level of the lock for managed application definition.</span></span>

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

### <span data-ttu-id="513b5-129">-MainTemplate</span><span class="sxs-lookup"><span data-stu-id="513b5-129">-MainTemplate</span></span>
<span data-ttu-id="513b5-130">受管理的應用程式定義主範本</span><span class="sxs-lookup"><span data-stu-id="513b5-130">The managed application definition main template</span></span>

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

### <span data-ttu-id="513b5-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="513b5-131">-Name</span></span>
<span data-ttu-id="513b5-132">受管理的應用程式定義名稱。</span><span class="sxs-lookup"><span data-stu-id="513b5-132">The managed application definition name.</span></span>

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

### <span data-ttu-id="513b5-133">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="513b5-133">-PackageFileUri</span></span>
<span data-ttu-id="513b5-134">受管理的應用程式定義套件檔案 uri。</span><span class="sxs-lookup"><span data-stu-id="513b5-134">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="513b5-135">-預先</span><span class="sxs-lookup"><span data-stu-id="513b5-135">-Pre</span></span>
<span data-ttu-id="513b5-136">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="513b5-136">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="513b5-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="513b5-137">-ResourceGroupName</span></span>
<span data-ttu-id="513b5-138">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="513b5-138">The resource group name.</span></span>

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

### <span data-ttu-id="513b5-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="513b5-139">-Tag</span></span>
<span data-ttu-id="513b5-140">代表資源標記的 hashtable。</span><span class="sxs-lookup"><span data-stu-id="513b5-140">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="513b5-141">-確認</span><span class="sxs-lookup"><span data-stu-id="513b5-141">-Confirm</span></span>
<span data-ttu-id="513b5-142">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="513b5-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="513b5-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="513b5-143">-WhatIf</span></span>
<span data-ttu-id="513b5-144">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="513b5-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="513b5-145">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="513b5-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="513b5-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="513b5-146">CommonParameters</span></span>
<span data-ttu-id="513b5-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="513b5-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="513b5-148">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="513b5-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="513b5-149">輸入</span><span class="sxs-lookup"><span data-stu-id="513b5-149">INPUTS</span></span>

### <span data-ttu-id="513b5-150">System.object</span><span class="sxs-lookup"><span data-stu-id="513b5-150">System.String</span></span>

### <span data-ttu-id="513b5-151">ApplicationLockLevel 中的 [.] 命令。</span><span class="sxs-lookup"><span data-stu-id="513b5-151">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationLockLevel</span></span>

### <span data-ttu-id="513b5-152">System.object []</span><span class="sxs-lookup"><span data-stu-id="513b5-152">System.String[]</span></span>

### <span data-ttu-id="513b5-153">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="513b5-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="513b5-154">輸出</span><span class="sxs-lookup"><span data-stu-id="513b5-154">OUTPUTS</span></span>

### <span data-ttu-id="513b5-155">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="513b5-155">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="513b5-156">筆記</span><span class="sxs-lookup"><span data-stu-id="513b5-156">NOTES</span></span>

## <span data-ttu-id="513b5-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="513b5-157">RELATED LINKS</span></span>