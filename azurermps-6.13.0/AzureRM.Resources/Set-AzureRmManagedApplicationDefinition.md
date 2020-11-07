---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmManagedApplicationDefinition.md
ms.openlocfilehash: 762987f39c1529b1b2c6dbce3325666704fd57fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625750"
---
# <span data-ttu-id="e3a9c-101">Set-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="e3a9c-101">Set-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="e3a9c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e3a9c-102">SYNOPSIS</span></span>
<span data-ttu-id="e3a9c-103">更新受管理的應用程式定義</span><span class="sxs-lookup"><span data-stu-id="e3a9c-103">Updates managed application definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3a9c-104">句法</span><span class="sxs-lookup"><span data-stu-id="e3a9c-104">SYNTAX</span></span>

### <span data-ttu-id="e3a9c-105">SetByNameAndResourceGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="e3a9c-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzureRmManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-DisplayName <String>]
 [-Description <String>] [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e3a9c-106">SetById</span><span class="sxs-lookup"><span data-stu-id="e3a9c-106">SetById</span></span>
```
Set-AzureRmManagedApplicationDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3a9c-107">說明</span><span class="sxs-lookup"><span data-stu-id="e3a9c-107">DESCRIPTION</span></span>
<span data-ttu-id="e3a9c-108">**AzureRmManagedApplicationDefinition** Cmdlet 會更新受管理的應用程式定義</span><span class="sxs-lookup"><span data-stu-id="e3a9c-108">The **Set-AzureRmManagedApplicationDefinition** cmdlet updates managed application definitions</span></span>

## <span data-ttu-id="e3a9c-109">示例</span><span class="sxs-lookup"><span data-stu-id="e3a9c-109">EXAMPLES</span></span>

### <span data-ttu-id="e3a9c-110">範例1：更新受管理的應用程式定義描述</span><span class="sxs-lookup"><span data-stu-id="e3a9c-110">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzureRmManagedApplicationDefinition -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applicationDefinitions/myAppDef" -Description "Updated description here"
```

<span data-ttu-id="e3a9c-111">這個命令會更新受管理的應用程式定義描述</span><span class="sxs-lookup"><span data-stu-id="e3a9c-111">This command updates the managed application definition description</span></span>

## <span data-ttu-id="e3a9c-112">參數</span><span class="sxs-lookup"><span data-stu-id="e3a9c-112">PARAMETERS</span></span>

### <span data-ttu-id="e3a9c-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e3a9c-113">-ApiVersion</span></span>
<span data-ttu-id="e3a9c-114">設定時，會指出要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="e3a9c-114">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="e3a9c-115">如果未指定，API 版本會自動決定為最新的可用。</span><span class="sxs-lookup"><span data-stu-id="e3a9c-115">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="e3a9c-116">-授權</span><span class="sxs-lookup"><span data-stu-id="e3a9c-116">-Authorization</span></span>
<span data-ttu-id="e3a9c-117">受管理的應用程式定義授權。</span><span class="sxs-lookup"><span data-stu-id="e3a9c-117">The managed application definition authorization.</span></span>
<span data-ttu-id="e3a9c-118">以逗號分隔授權對的格式 \<principalId\> ：\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="e3a9c-118">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3a9c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3a9c-119">-DefaultProfile</span></span>
<span data-ttu-id="e3a9c-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e3a9c-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3a9c-121">-描述</span><span class="sxs-lookup"><span data-stu-id="e3a9c-121">-Description</span></span>
<span data-ttu-id="e3a9c-122">受管理的應用程式定義說明。</span><span class="sxs-lookup"><span data-stu-id="e3a9c-122">The managed application definition description.</span></span>

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

### <span data-ttu-id="e3a9c-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e3a9c-123">-DisplayName</span></span>
<span data-ttu-id="e3a9c-124">受管理的應用程式定義顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="e3a9c-124">The managed application definition display name.</span></span>

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

### <span data-ttu-id="e3a9c-125">-識別碼</span><span class="sxs-lookup"><span data-stu-id="e3a9c-125">-Id</span></span>
<span data-ttu-id="e3a9c-126">完全限定的管理應用程式定義識別碼，包括訂閱。</span><span class="sxs-lookup"><span data-stu-id="e3a9c-126">The fully qualified managed application definition Id, including the subscription.</span></span> <span data-ttu-id="e3a9c-127">例如/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3a9c-127">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span></span>

```yaml
Type: System.String
Parameter Sets: SetById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3a9c-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="e3a9c-128">-Name</span></span>
<span data-ttu-id="e3a9c-129">受管理的應用程式定義名稱。</span><span class="sxs-lookup"><span data-stu-id="e3a9c-129">The managed application definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3a9c-130">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="e3a9c-130">-PackageFileUri</span></span>
<span data-ttu-id="e3a9c-131">受管理的應用程式定義套件檔案 uri。</span><span class="sxs-lookup"><span data-stu-id="e3a9c-131">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="e3a9c-132">-預先</span><span class="sxs-lookup"><span data-stu-id="e3a9c-132">-Pre</span></span>
<span data-ttu-id="e3a9c-133">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="e3a9c-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="e3a9c-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3a9c-134">-ResourceGroupName</span></span>
<span data-ttu-id="e3a9c-135">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e3a9c-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3a9c-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="e3a9c-136">-Tag</span></span>
<span data-ttu-id="e3a9c-137">代表資源標記的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="e3a9c-137">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="e3a9c-138">-確認</span><span class="sxs-lookup"><span data-stu-id="e3a9c-138">-Confirm</span></span>
<span data-ttu-id="e3a9c-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e3a9c-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3a9c-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3a9c-140">-WhatIf</span></span>
<span data-ttu-id="e3a9c-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e3a9c-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3a9c-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e3a9c-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3a9c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3a9c-143">CommonParameters</span></span>
<span data-ttu-id="e3a9c-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e3a9c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3a9c-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e3a9c-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3a9c-146">輸入</span><span class="sxs-lookup"><span data-stu-id="e3a9c-146">INPUTS</span></span>

### <span data-ttu-id="e3a9c-147">System.object</span><span class="sxs-lookup"><span data-stu-id="e3a9c-147">System.String</span></span>

### <span data-ttu-id="e3a9c-148">System.object []</span><span class="sxs-lookup"><span data-stu-id="e3a9c-148">System.String[]</span></span>

### <span data-ttu-id="e3a9c-149">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e3a9c-149">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e3a9c-150">輸出</span><span class="sxs-lookup"><span data-stu-id="e3a9c-150">OUTPUTS</span></span>

### <span data-ttu-id="e3a9c-151">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="e3a9c-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="e3a9c-152">筆記</span><span class="sxs-lookup"><span data-stu-id="e3a9c-152">NOTES</span></span>

## <span data-ttu-id="e3a9c-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="e3a9c-153">RELATED LINKS</span></span>
