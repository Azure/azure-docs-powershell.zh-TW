---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 0ea35e2f687308690107df5f92649dbbbeccdbaf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965784"
---
# <span data-ttu-id="6966c-101">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="6966c-101">New-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="6966c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6966c-102">SYNOPSIS</span></span>
<span data-ttu-id="6966c-103">建立整合帳戶元件。</span><span class="sxs-lookup"><span data-stu-id="6966c-103">Creates an integration account assembly.</span></span>

## <span data-ttu-id="6966c-104">句法</span><span class="sxs-lookup"><span data-stu-id="6966c-104">SYNTAX</span></span>

### <span data-ttu-id="6966c-105">ByIntegrationAccountAndFilePath (預設) </span><span class="sxs-lookup"><span data-stu-id="6966c-105">ByIntegrationAccountAndFilePath (Default)</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6966c-106">ByIntegrationAccountAndContentLink</span><span class="sxs-lookup"><span data-stu-id="6966c-106">ByIntegrationAccountAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -ContentLink <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6966c-107">ByIntegrationAccountAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="6966c-107">ByIntegrationAccountAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyData <Byte[]> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6966c-108">ByInputObjectAndContentLink</span><span class="sxs-lookup"><span data-stu-id="6966c-108">ByInputObjectAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6966c-109">ByInputObjectAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="6966c-109">ByInputObjectAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6966c-110">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="6966c-110">ByInputObjectAndFilePath</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6966c-111">ByResourceIdAndContentLink</span><span class="sxs-lookup"><span data-stu-id="6966c-111">ByResourceIdAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6966c-112">ByResourceIdAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="6966c-112">ByResourceIdAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6966c-113">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="6966c-113">ByResourceIdAndFilePath</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6966c-114">說明</span><span class="sxs-lookup"><span data-stu-id="6966c-114">DESCRIPTION</span></span>
<span data-ttu-id="6966c-115">**AzIntegrationAccountAssembly** Cmdlet 會在整合帳戶中建立新的元件。</span><span class="sxs-lookup"><span data-stu-id="6966c-115">The **Get-AzIntegrationAccountAssembly** cmdlet creates a new assembly in an integration account.</span></span>

## <span data-ttu-id="6966c-116">示例</span><span class="sxs-lookup"><span data-stu-id="6966c-116">EXAMPLES</span></span>

### <span data-ttu-id="6966c-117">範例1：使用本機檔案建立新的元件</span><span class="sxs-lookup"><span data-stu-id="6966c-117">Example 1: Create new assembly using local file</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyFilePath $localAssemblyFilePath

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="6966c-118">使用位於 [$localAssemblyFilePath] 中所含檔案路徑的本機檔案建立新的元件。</span><span class="sxs-lookup"><span data-stu-id="6966c-118">Creates a new assembly using the local file located at the file path contained in "$localAssemblyFilePath".</span></span>

### <span data-ttu-id="6966c-119">範例2：使用位元組資料建立新的元件</span><span class="sxs-lookup"><span data-stu-id="6966c-119">Example 2: Create new assembly using byte data</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyData $assemblyContent

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="6966c-120">使用「$assemblyContent」中所含的位元組陣列建立新的元件。</span><span class="sxs-lookup"><span data-stu-id="6966c-120">Creates a new assembly using the a byte array contained in "$assemblyContent".</span></span>

### <span data-ttu-id="6966c-121">範例3：使用內容連結建立新的元件</span><span class="sxs-lookup"><span data-stu-id="6966c-121">Example 3: Create new assembly using a content link</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -ContentLink $assemblyUrl

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="6966c-122">使用位於 URL "$assemblyUrl" 的位元組資料建立新的元件。</span><span class="sxs-lookup"><span data-stu-id="6966c-122">Creates a new assembly using the a byte data located at the URL "$assemblyUrl".</span></span> <span data-ttu-id="6966c-123">這是建立大型元件的建議方法。</span><span class="sxs-lookup"><span data-stu-id="6966c-123">This is the suggested method for creating large sized assemblies.</span></span>

## <span data-ttu-id="6966c-124">參數</span><span class="sxs-lookup"><span data-stu-id="6966c-124">PARAMETERS</span></span>

### <span data-ttu-id="6966c-125">-AssemblyData</span><span class="sxs-lookup"><span data-stu-id="6966c-125">-AssemblyData</span></span>
<span data-ttu-id="6966c-126">整合帳戶元件的位元組資料。</span><span class="sxs-lookup"><span data-stu-id="6966c-126">The integration account assembly byte data.</span></span>

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

### <span data-ttu-id="6966c-127">-AssemblyFilePath</span><span class="sxs-lookup"><span data-stu-id="6966c-127">-AssemblyFilePath</span></span>
<span data-ttu-id="6966c-128">整合帳戶元件的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="6966c-128">The integration account assembly file path.</span></span>

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

### <span data-ttu-id="6966c-129">-ContentLink</span><span class="sxs-lookup"><span data-stu-id="6966c-129">-ContentLink</span></span>
<span data-ttu-id="6966c-130">整合帳戶元件資料的公開存取連結。</span><span class="sxs-lookup"><span data-stu-id="6966c-130">A publicly accessible link to the integration account assembly data.</span></span>

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

### <span data-ttu-id="6966c-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6966c-131">-DefaultProfile</span></span>
<span data-ttu-id="6966c-132">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6966c-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6966c-133">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="6966c-133">-Metadata</span></span>
<span data-ttu-id="6966c-134">整合帳戶元件中繼資料。</span><span class="sxs-lookup"><span data-stu-id="6966c-134">The integration account assembly metadata.</span></span>

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

### <span data-ttu-id="6966c-135">-名稱</span><span class="sxs-lookup"><span data-stu-id="6966c-135">-Name</span></span>
<span data-ttu-id="6966c-136">整合帳戶元件名稱。</span><span class="sxs-lookup"><span data-stu-id="6966c-136">The integration account assembly name.</span></span>

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

### <span data-ttu-id="6966c-137">-ParentName</span><span class="sxs-lookup"><span data-stu-id="6966c-137">-ParentName</span></span>
<span data-ttu-id="6966c-138">整合帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="6966c-138">The integration account name.</span></span>

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

### <span data-ttu-id="6966c-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="6966c-139">-ParentObject</span></span>
<span data-ttu-id="6966c-140">整合帳戶物件。</span><span class="sxs-lookup"><span data-stu-id="6966c-140">An integration account object.</span></span>

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

### <span data-ttu-id="6966c-141">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="6966c-141">-ParentResourceId</span></span>
<span data-ttu-id="6966c-142">整合帳戶資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="6966c-142">The integration account resource id.</span></span>

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

### <span data-ttu-id="6966c-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6966c-143">-ResourceGroupName</span></span>
<span data-ttu-id="6966c-144">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6966c-144">The resource group name.</span></span>

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

### <span data-ttu-id="6966c-145">-確認</span><span class="sxs-lookup"><span data-stu-id="6966c-145">-Confirm</span></span>
<span data-ttu-id="6966c-146">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6966c-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6966c-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6966c-147">-WhatIf</span></span>
<span data-ttu-id="6966c-148">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6966c-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6966c-149">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6966c-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6966c-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6966c-150">CommonParameters</span></span>
<span data-ttu-id="6966c-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6966c-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6966c-152">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6966c-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6966c-153">輸入</span><span class="sxs-lookup"><span data-stu-id="6966c-153">INPUTS</span></span>

### <span data-ttu-id="6966c-154">IntegrationAccount 的管理邏輯。</span><span class="sxs-lookup"><span data-stu-id="6966c-154">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="6966c-155">System.object</span><span class="sxs-lookup"><span data-stu-id="6966c-155">System.String</span></span>

## <span data-ttu-id="6966c-156">輸出</span><span class="sxs-lookup"><span data-stu-id="6966c-156">OUTPUTS</span></span>

### <span data-ttu-id="6966c-157">PSIntegrationAccountAssembly 中的 LogicApp。</span><span class="sxs-lookup"><span data-stu-id="6966c-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="6966c-158">筆記</span><span class="sxs-lookup"><span data-stu-id="6966c-158">NOTES</span></span>

## <span data-ttu-id="6966c-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="6966c-159">RELATED LINKS</span></span>