---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-Azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzManagedApplicationDefinition.md
ms.openlocfilehash: 3d6a5488e7e101c904e90d056c8b2ffc03e786fb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795206"
---
# <span data-ttu-id="160b4-101">Set-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="160b4-101">Set-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="160b4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="160b4-102">SYNOPSIS</span></span>
<span data-ttu-id="160b4-103">更新受管理的應用程式定義</span><span class="sxs-lookup"><span data-stu-id="160b4-103">Updates managed application definition</span></span>

## <span data-ttu-id="160b4-104">句法</span><span class="sxs-lookup"><span data-stu-id="160b4-104">SYNTAX</span></span>

### <span data-ttu-id="160b4-105">SetByNameAndResourceGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="160b4-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-DisplayName <String>]
 [-Description <String>] [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="160b4-106">SetById</span><span class="sxs-lookup"><span data-stu-id="160b4-106">SetById</span></span>
```
Set-AzManagedApplicationDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="160b4-107">說明</span><span class="sxs-lookup"><span data-stu-id="160b4-107">DESCRIPTION</span></span>
<span data-ttu-id="160b4-108">**AzManagedApplicationDefinition** Cmdlet 會更新受管理的應用程式定義</span><span class="sxs-lookup"><span data-stu-id="160b4-108">The **Set-AzManagedApplicationDefinition** cmdlet updates managed application definitions</span></span>

## <span data-ttu-id="160b4-109">示例</span><span class="sxs-lookup"><span data-stu-id="160b4-109">EXAMPLES</span></span>

### <span data-ttu-id="160b4-110">範例1：更新受管理的應用程式定義描述</span><span class="sxs-lookup"><span data-stu-id="160b4-110">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzManagedApplicationDefinition -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applicationDefinitions/myAppDef" -Description "Updated description here"
```

<span data-ttu-id="160b4-111">這個命令會更新受管理的應用程式定義描述</span><span class="sxs-lookup"><span data-stu-id="160b4-111">This command updates the managed application definition description</span></span>

## <span data-ttu-id="160b4-112">參數</span><span class="sxs-lookup"><span data-stu-id="160b4-112">PARAMETERS</span></span>

### <span data-ttu-id="160b4-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="160b4-113">-ApiVersion</span></span>
<span data-ttu-id="160b4-114">設定時，會指出要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="160b4-114">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="160b4-115">如果未指定，API 版本會自動決定為最新的可用。</span><span class="sxs-lookup"><span data-stu-id="160b4-115">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="160b4-116">-授權</span><span class="sxs-lookup"><span data-stu-id="160b4-116">-Authorization</span></span>
<span data-ttu-id="160b4-117">受管理的應用程式定義授權。</span><span class="sxs-lookup"><span data-stu-id="160b4-117">The managed application definition authorization.</span></span>
<span data-ttu-id="160b4-118">以逗號分隔的授權對，格式為 \< principalId \> ： \< roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="160b4-118">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

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

### <span data-ttu-id="160b4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="160b4-119">-DefaultProfile</span></span>
<span data-ttu-id="160b4-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="160b4-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="160b4-121">-描述</span><span class="sxs-lookup"><span data-stu-id="160b4-121">-Description</span></span>
<span data-ttu-id="160b4-122">受管理的應用程式定義說明。</span><span class="sxs-lookup"><span data-stu-id="160b4-122">The managed application definition description.</span></span>

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

### <span data-ttu-id="160b4-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="160b4-123">-DisplayName</span></span>
<span data-ttu-id="160b4-124">受管理的應用程式定義顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="160b4-124">The managed application definition display name.</span></span>

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

### <span data-ttu-id="160b4-125">-識別碼</span><span class="sxs-lookup"><span data-stu-id="160b4-125">-Id</span></span>
<span data-ttu-id="160b4-126">完全限定的管理應用程式定義識別碼，包括訂閱。</span><span class="sxs-lookup"><span data-stu-id="160b4-126">The fully qualified managed application definition Id, including the subscription.</span></span> <span data-ttu-id="160b4-127">例如/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="160b4-127">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span></span>

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

### <span data-ttu-id="160b4-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="160b4-128">-Name</span></span>
<span data-ttu-id="160b4-129">受管理的應用程式定義名稱。</span><span class="sxs-lookup"><span data-stu-id="160b4-129">The managed application definition name.</span></span>

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

### <span data-ttu-id="160b4-130">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="160b4-130">-PackageFileUri</span></span>
<span data-ttu-id="160b4-131">受管理的應用程式定義套件檔案 uri。</span><span class="sxs-lookup"><span data-stu-id="160b4-131">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="160b4-132">-預先</span><span class="sxs-lookup"><span data-stu-id="160b4-132">-Pre</span></span>
<span data-ttu-id="160b4-133">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="160b4-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="160b4-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="160b4-134">-ResourceGroupName</span></span>
<span data-ttu-id="160b4-135">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="160b4-135">The resource group name.</span></span>

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

### <span data-ttu-id="160b4-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="160b4-136">-Tag</span></span>
<span data-ttu-id="160b4-137">代表資源標記的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="160b4-137">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="160b4-138">-確認</span><span class="sxs-lookup"><span data-stu-id="160b4-138">-Confirm</span></span>
<span data-ttu-id="160b4-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="160b4-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="160b4-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="160b4-140">-WhatIf</span></span>
<span data-ttu-id="160b4-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="160b4-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="160b4-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="160b4-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="160b4-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="160b4-143">CommonParameters</span></span>
<span data-ttu-id="160b4-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="160b4-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="160b4-145">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="160b4-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="160b4-146">輸入</span><span class="sxs-lookup"><span data-stu-id="160b4-146">INPUTS</span></span>

### <span data-ttu-id="160b4-147">System.object</span><span class="sxs-lookup"><span data-stu-id="160b4-147">System.String</span></span>

### <span data-ttu-id="160b4-148">System.object []</span><span class="sxs-lookup"><span data-stu-id="160b4-148">System.String[]</span></span>

### <span data-ttu-id="160b4-149">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="160b4-149">System.Collections.Hashtable</span></span>

## <span data-ttu-id="160b4-150">輸出</span><span class="sxs-lookup"><span data-stu-id="160b4-150">OUTPUTS</span></span>

### <span data-ttu-id="160b4-151">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="160b4-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="160b4-152">筆記</span><span class="sxs-lookup"><span data-stu-id="160b4-152">NOTES</span></span>

## <span data-ttu-id="160b4-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="160b4-153">RELATED LINKS</span></span>
