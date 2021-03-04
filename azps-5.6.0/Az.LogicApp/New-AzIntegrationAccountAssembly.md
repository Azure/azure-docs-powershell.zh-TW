---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/powershell/module/az.logicapp/new-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAssembly.md
ms.openlocfilehash: a52d1d44647d2b608a34a07722439f243ba08510
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916530"
---
# <span data-ttu-id="4b876-101">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="4b876-101">New-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="4b876-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4b876-102">SYNOPSIS</span></span>
<span data-ttu-id="4b876-103">建立整合帳戶元件。</span><span class="sxs-lookup"><span data-stu-id="4b876-103">Creates an integration account assembly.</span></span>

## <span data-ttu-id="4b876-104">語法</span><span class="sxs-lookup"><span data-stu-id="4b876-104">SYNTAX</span></span>

### <span data-ttu-id="4b876-105">By方AccountAndFilePath (預設) </span><span class="sxs-lookup"><span data-stu-id="4b876-105">ByIntegrationAccountAndFilePath (Default)</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b876-106">ByTentAccountAndContentLink</span><span class="sxs-lookup"><span data-stu-id="4b876-106">ByIntegrationAccountAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -ContentLink <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4b876-107">By方AccountAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="4b876-107">ByIntegrationAccountAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyData <Byte[]> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4b876-108">ByInputObjectAndContentLink</span><span class="sxs-lookup"><span data-stu-id="4b876-108">ByInputObjectAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b876-109">ByInputObjectAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="4b876-109">ByInputObjectAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b876-110">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="4b876-110">ByInputObjectAndFilePath</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b876-111">ByResourceIdAndContentLink</span><span class="sxs-lookup"><span data-stu-id="4b876-111">ByResourceIdAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b876-112">ByResourceIdAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="4b876-112">ByResourceIdAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b876-113">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="4b876-113">ByResourceIdAndFilePath</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b876-114">描述</span><span class="sxs-lookup"><span data-stu-id="4b876-114">DESCRIPTION</span></span>
<span data-ttu-id="4b876-115">**Get-AzAsseAccountAssembly** Cmdlet 在整合帳戶中建立新元件。</span><span class="sxs-lookup"><span data-stu-id="4b876-115">The **Get-AzIntegrationAccountAssembly** cmdlet creates a new assembly in an integration account.</span></span>

## <span data-ttu-id="4b876-116">例子</span><span class="sxs-lookup"><span data-stu-id="4b876-116">EXAMPLES</span></span>

### <span data-ttu-id="4b876-117">範例 1：使用本地檔案建立新元件</span><span class="sxs-lookup"><span data-stu-id="4b876-117">Example 1: Create new assembly using local file</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyFilePath $localAssemblyFilePath

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="4b876-118">使用位於「$localAssemblyFilePath」中包含的檔案路徑的本地檔案來建立新元件。</span><span class="sxs-lookup"><span data-stu-id="4b876-118">Creates a new assembly using the local file located at the file path contained in "$localAssemblyFilePath".</span></span>

### <span data-ttu-id="4b876-119">範例 2：使用位元組資料建立新元件</span><span class="sxs-lookup"><span data-stu-id="4b876-119">Example 2: Create new assembly using byte data</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyData $assemblyContent

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="4b876-120">使用 "$assemblyContent" 中包含的位元組陣列來建立新元件。</span><span class="sxs-lookup"><span data-stu-id="4b876-120">Creates a new assembly using the a byte array contained in "$assemblyContent".</span></span>

### <span data-ttu-id="4b876-121">範例 3：使用內容連結建立新元件</span><span class="sxs-lookup"><span data-stu-id="4b876-121">Example 3: Create new assembly using a content link</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -ContentLink $assemblyUrl

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="4b876-122">使用位於 URL "$assemblyUrl" 的位元組資料來建立新元件。</span><span class="sxs-lookup"><span data-stu-id="4b876-122">Creates a new assembly using the a byte data located at the URL "$assemblyUrl".</span></span> <span data-ttu-id="4b876-123">這是建立大型元件的建議方法。</span><span class="sxs-lookup"><span data-stu-id="4b876-123">This is the suggested method for creating large sized assemblies.</span></span>

## <span data-ttu-id="4b876-124">參數</span><span class="sxs-lookup"><span data-stu-id="4b876-124">PARAMETERS</span></span>

### <span data-ttu-id="4b876-125">-程式集資料</span><span class="sxs-lookup"><span data-stu-id="4b876-125">-AssemblyData</span></span>
<span data-ttu-id="4b876-126">整合帳戶元件位元組資料。</span><span class="sxs-lookup"><span data-stu-id="4b876-126">The integration account assembly byte data.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: ByIntegrationAccountAndFileBytes, ByInputObjectAndFileBytes, ByResourceIdAndFileBytes
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b876-127">-AssemblyFilePath</span><span class="sxs-lookup"><span data-stu-id="4b876-127">-AssemblyFilePath</span></span>
<span data-ttu-id="4b876-128">整合帳戶元件檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="4b876-128">The integration account assembly file path.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndFilePath, ByInputObjectAndFilePath, ByResourceIdAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b876-129">-ContentLink</span><span class="sxs-lookup"><span data-stu-id="4b876-129">-ContentLink</span></span>
<span data-ttu-id="4b876-130">可公開連結至整合帳戶元件資料。</span><span class="sxs-lookup"><span data-stu-id="4b876-130">A publicly accessible link to the integration account assembly data.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndContentLink, ByInputObjectAndContentLink, ByResourceIdAndContentLink
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b876-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b876-131">-DefaultProfile</span></span>
<span data-ttu-id="4b876-132">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4b876-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b876-133">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="4b876-133">-Metadata</span></span>
<span data-ttu-id="4b876-134">整合帳戶元件中繼資料。</span><span class="sxs-lookup"><span data-stu-id="4b876-134">The integration account assembly metadata.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b876-135">-名稱</span><span class="sxs-lookup"><span data-stu-id="4b876-135">-Name</span></span>
<span data-ttu-id="4b876-136">整合帳戶元件名稱。</span><span class="sxs-lookup"><span data-stu-id="4b876-136">The integration account assembly name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AssemblyName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b876-137">-ParentName</span><span class="sxs-lookup"><span data-stu-id="4b876-137">-ParentName</span></span>
<span data-ttu-id="4b876-138">整合帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="4b876-138">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndFilePath, ByIntegrationAccountAndContentLink, ByIntegrationAccountAndFileBytes
Aliases: IntegrationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b876-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4b876-139">-ParentObject</span></span>
<span data-ttu-id="4b876-140">整合帳戶物件。</span><span class="sxs-lookup"><span data-stu-id="4b876-140">An integration account object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Logic.Models.IntegrationAccount
Parameter Sets: ByInputObjectAndContentLink, ByInputObjectAndFileBytes, ByInputObjectAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4b876-141">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4b876-141">-ParentResourceId</span></span>
<span data-ttu-id="4b876-142">整合帳戶資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="4b876-142">The integration account resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdAndContentLink, ByResourceIdAndFileBytes, ByResourceIdAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b876-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b876-143">-ResourceGroupName</span></span>
<span data-ttu-id="4b876-144">資源組名。</span><span class="sxs-lookup"><span data-stu-id="4b876-144">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndFilePath, ByIntegrationAccountAndContentLink, ByIntegrationAccountAndFileBytes
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b876-145">-確認</span><span class="sxs-lookup"><span data-stu-id="4b876-145">-Confirm</span></span>
<span data-ttu-id="4b876-146">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="4b876-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b876-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b876-147">-WhatIf</span></span>
<span data-ttu-id="4b876-148">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4b876-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4b876-149">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4b876-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b876-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b876-150">CommonParameters</span></span>
<span data-ttu-id="4b876-151">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4b876-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b876-152">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="4b876-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b876-153">輸入</span><span class="sxs-lookup"><span data-stu-id="4b876-153">INPUTS</span></span>

### <span data-ttu-id="4b876-154">Microsoft.Azure.management.Logic.models.IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="4b876-154">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="4b876-155">System.String</span><span class="sxs-lookup"><span data-stu-id="4b876-155">System.String</span></span>

## <span data-ttu-id="4b876-156">輸出</span><span class="sxs-lookup"><span data-stu-id="4b876-156">OUTPUTS</span></span>

### <span data-ttu-id="4b876-157">Microsoft.Azure.Commands.LogicApp.models.PSAsseAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="4b876-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="4b876-158">筆記</span><span class="sxs-lookup"><span data-stu-id="4b876-158">NOTES</span></span>

## <span data-ttu-id="4b876-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="4b876-159">RELATED LINKS</span></span>
