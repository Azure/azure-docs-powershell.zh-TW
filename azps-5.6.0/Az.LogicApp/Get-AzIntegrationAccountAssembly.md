---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 95daa8025dde470e85d0e00e09c00f26d08e1342
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916401"
---
# <span data-ttu-id="98e5e-101">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="98e5e-101">Get-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="98e5e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="98e5e-102">SYNOPSIS</span></span>
<span data-ttu-id="98e5e-103">獲得整合帳戶元件。</span><span class="sxs-lookup"><span data-stu-id="98e5e-103">Gets an integration account assembly.</span></span>

## <span data-ttu-id="98e5e-104">語法</span><span class="sxs-lookup"><span data-stu-id="98e5e-104">SYNTAX</span></span>

### <span data-ttu-id="98e5e-105">By方Account (預設) </span><span class="sxs-lookup"><span data-stu-id="98e5e-105">ByIntegrationAccount (Default)</span></span>
```
Get-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98e5e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="98e5e-106">ByInputObject</span></span>
```
Get-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98e5e-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="98e5e-107">ByResourceId</span></span>
```
Get-AzIntegrationAccountAssembly -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98e5e-108">描述</span><span class="sxs-lookup"><span data-stu-id="98e5e-108">DESCRIPTION</span></span>
<span data-ttu-id="98e5e-109">**Get-AzAsseCountAssembly** Cmdlet 會從整合帳戶取得一個元件。</span><span class="sxs-lookup"><span data-stu-id="98e5e-109">The **Get-AzIntegrationAccountAssembly** cmdlet gets an assembly from an integration account.</span></span>

## <span data-ttu-id="98e5e-110">例子</span><span class="sxs-lookup"><span data-stu-id="98e5e-110">EXAMPLES</span></span>

### <span data-ttu-id="98e5e-111">範例 1：根據參數取得元件</span><span class="sxs-lookup"><span data-stu-id="98e5e-111">Example 1: Get an assembly by parameters</span></span>
```powershell
PS C:\> Get-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly"

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="98e5e-112">取得名稱為"sampleAssembly"的程式集，位於整合帳戶 "sampleAsseAccount" 中，此元件包含在資源群組"sampleResourceGroup"中。</span><span class="sxs-lookup"><span data-stu-id="98e5e-112">Get an assembly named "sampleAssembly" located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

### <span data-ttu-id="98e5e-113">範例 2：根據參數列出整合帳戶中的所有元件</span><span class="sxs-lookup"><span data-stu-id="98e5e-113">Example 2: List all assemblies in an integration account by parameters</span></span>
```powershell
PS C:\> Get-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount"

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly2
Name       : sampleAssembly2
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="98e5e-114">取得位於整合帳戶 "sample準備Account"的所有元件，此元件包含在資源群組"sampleResourceGroup"中。</span><span class="sxs-lookup"><span data-stu-id="98e5e-114">Get all assemblies located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

## <span data-ttu-id="98e5e-115">參數</span><span class="sxs-lookup"><span data-stu-id="98e5e-115">PARAMETERS</span></span>

### <span data-ttu-id="98e5e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98e5e-116">-DefaultProfile</span></span>
<span data-ttu-id="98e5e-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="98e5e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98e5e-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="98e5e-118">-Name</span></span>
<span data-ttu-id="98e5e-119">整合帳戶元件名稱。</span><span class="sxs-lookup"><span data-stu-id="98e5e-119">The integration account assembly name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AssemblyName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98e5e-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="98e5e-120">-ParentName</span></span>
<span data-ttu-id="98e5e-121">整合帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="98e5e-121">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases: IntegrationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98e5e-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="98e5e-122">-ParentObject</span></span>
<span data-ttu-id="98e5e-123">整合帳戶物件。</span><span class="sxs-lookup"><span data-stu-id="98e5e-123">An integration account object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Logic.Models.IntegrationAccount
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98e5e-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="98e5e-124">-ParentResourceId</span></span>
<span data-ttu-id="98e5e-125">整合帳戶資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="98e5e-125">The integration account resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98e5e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98e5e-126">-ResourceGroupName</span></span>
<span data-ttu-id="98e5e-127">資源組名。</span><span class="sxs-lookup"><span data-stu-id="98e5e-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98e5e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98e5e-128">CommonParameters</span></span>
<span data-ttu-id="98e5e-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="98e5e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98e5e-130">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="98e5e-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98e5e-131">輸入</span><span class="sxs-lookup"><span data-stu-id="98e5e-131">INPUTS</span></span>

### <span data-ttu-id="98e5e-132">Microsoft.Azure.management.Logic.models.IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="98e5e-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="98e5e-133">System.String</span><span class="sxs-lookup"><span data-stu-id="98e5e-133">System.String</span></span>

## <span data-ttu-id="98e5e-134">輸出</span><span class="sxs-lookup"><span data-stu-id="98e5e-134">OUTPUTS</span></span>

### <span data-ttu-id="98e5e-135">Microsoft.Azure.Commands.LogicApp.models.PSAsseAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="98e5e-135">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="98e5e-136">筆記</span><span class="sxs-lookup"><span data-stu-id="98e5e-136">NOTES</span></span>

## <span data-ttu-id="98e5e-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="98e5e-137">RELATED LINKS</span></span>
