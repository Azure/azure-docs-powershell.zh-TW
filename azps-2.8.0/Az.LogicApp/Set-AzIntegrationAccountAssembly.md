---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAssembly.md
ms.openlocfilehash: a3f2c76de9dc331c6b073f724fede6a3bafeed18
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93611956"
---
# <span data-ttu-id="63e3d-101">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="63e3d-101">Set-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="63e3d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="63e3d-102">SYNOPSIS</span></span>
<span data-ttu-id="63e3d-103">修改整合帳戶元件。</span><span class="sxs-lookup"><span data-stu-id="63e3d-103">Modifies an integration account assembly.</span></span>

## <span data-ttu-id="63e3d-104">句法</span><span class="sxs-lookup"><span data-stu-id="63e3d-104">SYNTAX</span></span>

### <span data-ttu-id="63e3d-105">ByIntegrationAccountAndFilePath (預設) </span><span class="sxs-lookup"><span data-stu-id="63e3d-105">ByIntegrationAccountAndFilePath (Default)</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63e3d-106">ByIntegrationAccountAndContentLink</span><span class="sxs-lookup"><span data-stu-id="63e3d-106">ByIntegrationAccountAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -ContentLink <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="63e3d-107">ByIntegrationAccountAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="63e3d-107">ByIntegrationAccountAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyData <Byte[]> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="63e3d-108">ByInputObjectAndContentLink</span><span class="sxs-lookup"><span data-stu-id="63e3d-108">ByInputObjectAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63e3d-109">ByInputObjectAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="63e3d-109">ByInputObjectAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63e3d-110">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="63e3d-110">ByInputObjectAndFilePath</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63e3d-111">ByResourceIdAndContentLink</span><span class="sxs-lookup"><span data-stu-id="63e3d-111">ByResourceIdAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -ContentLink <String> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63e3d-112">ByResourceIdAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="63e3d-112">ByResourceIdAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -AssemblyData <Byte[]> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63e3d-113">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="63e3d-113">ByResourceIdAndFilePath</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -AssemblyFilePath <String> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63e3d-114">說明</span><span class="sxs-lookup"><span data-stu-id="63e3d-114">DESCRIPTION</span></span>
<span data-ttu-id="63e3d-115">**AzIntegrationAccountAssembly** Cmdlet 會修改整合帳戶元件。</span><span class="sxs-lookup"><span data-stu-id="63e3d-115">The **Set-AzIntegrationAccountAssembly** cmdlet modifies an integration account assembly.</span></span>

## <span data-ttu-id="63e3d-116">示例</span><span class="sxs-lookup"><span data-stu-id="63e3d-116">EXAMPLES</span></span>

### <span data-ttu-id="63e3d-117">範例1：使用本機檔案修改元件</span><span class="sxs-lookup"><span data-stu-id="63e3d-117">Example 1: Modify an assembly using local file</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyFilePath $localAssemblyFilePath

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="63e3d-118">使用位於 [$localAssemblyFilePath] 中所含檔案路徑的本機檔案，修改名為「sampleAssembly」的程式集。</span><span class="sxs-lookup"><span data-stu-id="63e3d-118">Modifies the assembly named "sampleAssembly" using the local file located at the file path contained in "$localAssemblyFilePath".</span></span>

### <span data-ttu-id="63e3d-119">範例2：使用位元組資料修改元件</span><span class="sxs-lookup"><span data-stu-id="63e3d-119">Example 2: Modify an assembly using byte data</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyData $assemblyContent

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="63e3d-120">使用「$assemblyContent」中所含的位元組陣列來修改名為「sampleAssembly」的程式集。</span><span class="sxs-lookup"><span data-stu-id="63e3d-120">Modifies the assembly named "sampleAssembly" using the a byte array contained in "$assemblyContent".</span></span>

### <span data-ttu-id="63e3d-121">範例3：使用內容連結修改元件</span><span class="sxs-lookup"><span data-stu-id="63e3d-121">Example 3: Modify an assembly using a content link</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -ContentLink $assemblyUrl

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="63e3d-122">使用位於 URL "$assemblyUrl" 的位元組資料來修改名為 "sampleAssembly" 的元件。</span><span class="sxs-lookup"><span data-stu-id="63e3d-122">Modifies the assembly named "sampleAssembly" using the a byte data located at the URL "$assemblyUrl".</span></span> <span data-ttu-id="63e3d-123">這是建立大型元件的建議方法。</span><span class="sxs-lookup"><span data-stu-id="63e3d-123">This is the suggested method for creating large sized assemblies.</span></span>

## <span data-ttu-id="63e3d-124">參數</span><span class="sxs-lookup"><span data-stu-id="63e3d-124">PARAMETERS</span></span>

### <span data-ttu-id="63e3d-125">-AssemblyData</span><span class="sxs-lookup"><span data-stu-id="63e3d-125">-AssemblyData</span></span>
<span data-ttu-id="63e3d-126">整合帳戶元件的位元組資料。</span><span class="sxs-lookup"><span data-stu-id="63e3d-126">The integration account assembly byte data.</span></span>

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

### <span data-ttu-id="63e3d-127">-AssemblyFilePath</span><span class="sxs-lookup"><span data-stu-id="63e3d-127">-AssemblyFilePath</span></span>
<span data-ttu-id="63e3d-128">整合帳戶元件的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="63e3d-128">The integration account assembly file path.</span></span>

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

### <span data-ttu-id="63e3d-129">-ContentLink</span><span class="sxs-lookup"><span data-stu-id="63e3d-129">-ContentLink</span></span>
<span data-ttu-id="63e3d-130">整合帳戶元件資料的公開存取連結。</span><span class="sxs-lookup"><span data-stu-id="63e3d-130">A publicly accessible link to the integration account assembly data.</span></span>

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

### <span data-ttu-id="63e3d-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63e3d-131">-DefaultProfile</span></span>
<span data-ttu-id="63e3d-132">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="63e3d-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63e3d-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="63e3d-133">-InputObject</span></span>
<span data-ttu-id="63e3d-134">整合帳戶元件。</span><span class="sxs-lookup"><span data-stu-id="63e3d-134">An integration account assembly.</span></span>

```yaml
Type: Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly
Parameter Sets: ByInputObjectAndContentLink, ByInputObjectAndFileBytes, ByInputObjectAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63e3d-135">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="63e3d-135">-Metadata</span></span>
<span data-ttu-id="63e3d-136">整合帳戶元件中繼資料。</span><span class="sxs-lookup"><span data-stu-id="63e3d-136">The integration account assembly metadata.</span></span>

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

### <span data-ttu-id="63e3d-137">-名稱</span><span class="sxs-lookup"><span data-stu-id="63e3d-137">-Name</span></span>
<span data-ttu-id="63e3d-138">整合帳戶元件名稱。</span><span class="sxs-lookup"><span data-stu-id="63e3d-138">The integration account assembly name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndFilePath, ByIntegrationAccountAndContentLink, ByIntegrationAccountAndFileBytes
Aliases: AssemblyName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63e3d-139">-ParentName</span><span class="sxs-lookup"><span data-stu-id="63e3d-139">-ParentName</span></span>
<span data-ttu-id="63e3d-140">整合帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="63e3d-140">The integration account name.</span></span>

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

### <span data-ttu-id="63e3d-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63e3d-141">-ResourceGroupName</span></span>
<span data-ttu-id="63e3d-142">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="63e3d-142">The resource group name.</span></span>

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

### <span data-ttu-id="63e3d-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="63e3d-143">-ResourceId</span></span>
<span data-ttu-id="63e3d-144">整合帳戶元件名稱資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="63e3d-144">The integration account assembly resource id.</span></span>

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

### <span data-ttu-id="63e3d-145">-確認</span><span class="sxs-lookup"><span data-stu-id="63e3d-145">-Confirm</span></span>
<span data-ttu-id="63e3d-146">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="63e3d-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63e3d-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63e3d-147">-WhatIf</span></span>
<span data-ttu-id="63e3d-148">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="63e3d-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="63e3d-149">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="63e3d-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63e3d-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63e3d-150">CommonParameters</span></span>
<span data-ttu-id="63e3d-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="63e3d-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63e3d-152">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="63e3d-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63e3d-153">輸入</span><span class="sxs-lookup"><span data-stu-id="63e3d-153">INPUTS</span></span>

### <span data-ttu-id="63e3d-154">PSIntegrationAccountAssembly 中的 LogicApp。</span><span class="sxs-lookup"><span data-stu-id="63e3d-154">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

### <span data-ttu-id="63e3d-155">System.object</span><span class="sxs-lookup"><span data-stu-id="63e3d-155">System.String</span></span>

## <span data-ttu-id="63e3d-156">輸出</span><span class="sxs-lookup"><span data-stu-id="63e3d-156">OUTPUTS</span></span>

### <span data-ttu-id="63e3d-157">PSIntegrationAccountAssembly 中的 LogicApp。</span><span class="sxs-lookup"><span data-stu-id="63e3d-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="63e3d-158">筆記</span><span class="sxs-lookup"><span data-stu-id="63e3d-158">NOTES</span></span>

## <span data-ttu-id="63e3d-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="63e3d-159">RELATED LINKS</span></span>