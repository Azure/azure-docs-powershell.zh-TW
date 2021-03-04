---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/powershell/module/az.logicapp/set-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 74531aa3c5e142cf3c9638f4910c8d45654a20f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911005"
---
# <span data-ttu-id="afba6-101">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="afba6-101">Set-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="afba6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="afba6-102">SYNOPSIS</span></span>
<span data-ttu-id="afba6-103">修改整合帳戶元件。</span><span class="sxs-lookup"><span data-stu-id="afba6-103">Modifies an integration account assembly.</span></span>

## <span data-ttu-id="afba6-104">語法</span><span class="sxs-lookup"><span data-stu-id="afba6-104">SYNTAX</span></span>

### <span data-ttu-id="afba6-105">By方AccountAndFilePath (預設) </span><span class="sxs-lookup"><span data-stu-id="afba6-105">ByIntegrationAccountAndFilePath (Default)</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afba6-106">ByTentAccountAndContentLink</span><span class="sxs-lookup"><span data-stu-id="afba6-106">ByIntegrationAccountAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -ContentLink <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="afba6-107">By方AccountAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="afba6-107">ByIntegrationAccountAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyData <Byte[]> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="afba6-108">ByInputObjectAndContentLink</span><span class="sxs-lookup"><span data-stu-id="afba6-108">ByInputObjectAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afba6-109">ByInputObjectAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="afba6-109">ByInputObjectAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afba6-110">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="afba6-110">ByInputObjectAndFilePath</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afba6-111">ByResourceIdAndContentLink</span><span class="sxs-lookup"><span data-stu-id="afba6-111">ByResourceIdAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -ContentLink <String> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afba6-112">ByResourceIdAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="afba6-112">ByResourceIdAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -AssemblyData <Byte[]> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afba6-113">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="afba6-113">ByResourceIdAndFilePath</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -AssemblyFilePath <String> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afba6-114">描述</span><span class="sxs-lookup"><span data-stu-id="afba6-114">DESCRIPTION</span></span>
<span data-ttu-id="afba6-115">**Set-AzAsseAccountAssembly** Cmdlet 會修改整合帳戶元件。</span><span class="sxs-lookup"><span data-stu-id="afba6-115">The **Set-AzIntegrationAccountAssembly** cmdlet modifies an integration account assembly.</span></span>

## <span data-ttu-id="afba6-116">例子</span><span class="sxs-lookup"><span data-stu-id="afba6-116">EXAMPLES</span></span>

### <span data-ttu-id="afba6-117">範例 1：使用本地檔案修改元件</span><span class="sxs-lookup"><span data-stu-id="afba6-117">Example 1: Modify an assembly using local file</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyFilePath $localAssemblyFilePath

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="afba6-118">使用位於 "$localAssemblyFilePath" 包含之檔案路徑的本地檔案來修改名為「sampleAssembly」的$localAssemblyFilePath。</span><span class="sxs-lookup"><span data-stu-id="afba6-118">Modifies the assembly named "sampleAssembly" using the local file located at the file path contained in "$localAssemblyFilePath".</span></span>

### <span data-ttu-id="afba6-119">範例 2：使用位元組資料修改元件</span><span class="sxs-lookup"><span data-stu-id="afba6-119">Example 2: Modify an assembly using byte data</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyData $assemblyContent

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="afba6-120">使用 "sampleAssembly" 中包含的位元組陣列來修改名為 "sampleAssembly" 的$assemblyContent。</span><span class="sxs-lookup"><span data-stu-id="afba6-120">Modifies the assembly named "sampleAssembly" using the a byte array contained in "$assemblyContent".</span></span>

### <span data-ttu-id="afba6-121">範例 3：使用內容連結修改元件</span><span class="sxs-lookup"><span data-stu-id="afba6-121">Example 3: Modify an assembly using a content link</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -ContentLink $assemblyUrl

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="afba6-122">使用位於 URL "$assemblyUrl" 的位元組資料來修改名為 "sampleAssembly" 的$assemblyUrl。</span><span class="sxs-lookup"><span data-stu-id="afba6-122">Modifies the assembly named "sampleAssembly" using the a byte data located at the URL "$assemblyUrl".</span></span> <span data-ttu-id="afba6-123">這是建立大型元件的建議方法。</span><span class="sxs-lookup"><span data-stu-id="afba6-123">This is the suggested method for creating large sized assemblies.</span></span>

## <span data-ttu-id="afba6-124">參數</span><span class="sxs-lookup"><span data-stu-id="afba6-124">PARAMETERS</span></span>

### <span data-ttu-id="afba6-125">-程式集資料</span><span class="sxs-lookup"><span data-stu-id="afba6-125">-AssemblyData</span></span>
<span data-ttu-id="afba6-126">整合帳戶元件位元組資料。</span><span class="sxs-lookup"><span data-stu-id="afba6-126">The integration account assembly byte data.</span></span>

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

### <span data-ttu-id="afba6-127">-AssemblyFilePath</span><span class="sxs-lookup"><span data-stu-id="afba6-127">-AssemblyFilePath</span></span>
<span data-ttu-id="afba6-128">整合帳戶元件檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="afba6-128">The integration account assembly file path.</span></span>

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

### <span data-ttu-id="afba6-129">-ContentLink</span><span class="sxs-lookup"><span data-stu-id="afba6-129">-ContentLink</span></span>
<span data-ttu-id="afba6-130">可公開連結至整合帳戶元件資料。</span><span class="sxs-lookup"><span data-stu-id="afba6-130">A publicly accessible link to the integration account assembly data.</span></span>

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

### <span data-ttu-id="afba6-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afba6-131">-DefaultProfile</span></span>
<span data-ttu-id="afba6-132">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="afba6-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afba6-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="afba6-133">-InputObject</span></span>
<span data-ttu-id="afba6-134">整合帳戶元件。</span><span class="sxs-lookup"><span data-stu-id="afba6-134">An integration account assembly.</span></span>

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

### <span data-ttu-id="afba6-135">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="afba6-135">-Metadata</span></span>
<span data-ttu-id="afba6-136">整合帳戶元件中繼資料。</span><span class="sxs-lookup"><span data-stu-id="afba6-136">The integration account assembly metadata.</span></span>

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

### <span data-ttu-id="afba6-137">-名稱</span><span class="sxs-lookup"><span data-stu-id="afba6-137">-Name</span></span>
<span data-ttu-id="afba6-138">整合帳戶元件名稱。</span><span class="sxs-lookup"><span data-stu-id="afba6-138">The integration account assembly name.</span></span>

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

### <span data-ttu-id="afba6-139">-ParentName</span><span class="sxs-lookup"><span data-stu-id="afba6-139">-ParentName</span></span>
<span data-ttu-id="afba6-140">整合帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="afba6-140">The integration account name.</span></span>

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

### <span data-ttu-id="afba6-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afba6-141">-ResourceGroupName</span></span>
<span data-ttu-id="afba6-142">資源組名。</span><span class="sxs-lookup"><span data-stu-id="afba6-142">The resource group name.</span></span>

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

### <span data-ttu-id="afba6-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="afba6-143">-ResourceId</span></span>
<span data-ttu-id="afba6-144">整合帳戶元件資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="afba6-144">The integration account assembly resource id.</span></span>

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

### <span data-ttu-id="afba6-145">-確認</span><span class="sxs-lookup"><span data-stu-id="afba6-145">-Confirm</span></span>
<span data-ttu-id="afba6-146">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="afba6-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afba6-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afba6-147">-WhatIf</span></span>
<span data-ttu-id="afba6-148">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="afba6-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="afba6-149">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="afba6-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afba6-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afba6-150">CommonParameters</span></span>
<span data-ttu-id="afba6-151">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="afba6-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afba6-152">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="afba6-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afba6-153">輸入</span><span class="sxs-lookup"><span data-stu-id="afba6-153">INPUTS</span></span>

### <span data-ttu-id="afba6-154">Microsoft.Azure.Commands.LogicApp.models.PSAsseAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="afba6-154">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

### <span data-ttu-id="afba6-155">System.String</span><span class="sxs-lookup"><span data-stu-id="afba6-155">System.String</span></span>

## <span data-ttu-id="afba6-156">輸出</span><span class="sxs-lookup"><span data-stu-id="afba6-156">OUTPUTS</span></span>

### <span data-ttu-id="afba6-157">Microsoft.Azure.Commands.LogicApp.models.PSAsseAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="afba6-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="afba6-158">筆記</span><span class="sxs-lookup"><span data-stu-id="afba6-158">NOTES</span></span>

## <span data-ttu-id="afba6-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="afba6-159">RELATED LINKS</span></span>
