---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 59b4ad9eb439808033233aa1677be16862c8a973
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127783"
---
# <span data-ttu-id="84a0c-101">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="84a0c-101">Get-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="84a0c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="84a0c-102">SYNOPSIS</span></span>
<span data-ttu-id="84a0c-103">取得整合帳戶元件。</span><span class="sxs-lookup"><span data-stu-id="84a0c-103">Gets an integration account assembly.</span></span>

## <span data-ttu-id="84a0c-104">句法</span><span class="sxs-lookup"><span data-stu-id="84a0c-104">SYNTAX</span></span>

### <span data-ttu-id="84a0c-105">ByIntegrationAccount (預設) </span><span class="sxs-lookup"><span data-stu-id="84a0c-105">ByIntegrationAccount (Default)</span></span>
```
Get-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84a0c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="84a0c-106">ByInputObject</span></span>
```
Get-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84a0c-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="84a0c-107">ByResourceId</span></span>
```
Get-AzIntegrationAccountAssembly -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84a0c-108">說明</span><span class="sxs-lookup"><span data-stu-id="84a0c-108">DESCRIPTION</span></span>
<span data-ttu-id="84a0c-109">**AzIntegrationAccountAssembly** Cmdlet 會從整合帳戶取得元件。</span><span class="sxs-lookup"><span data-stu-id="84a0c-109">The **Get-AzIntegrationAccountAssembly** cmdlet gets an assembly from an integration account.</span></span>

## <span data-ttu-id="84a0c-110">示例</span><span class="sxs-lookup"><span data-stu-id="84a0c-110">EXAMPLES</span></span>

### <span data-ttu-id="84a0c-111">範例1：透過參數取得元件</span><span class="sxs-lookup"><span data-stu-id="84a0c-111">Example 1: Get an assembly by parameters</span></span>
```powershell
PS C:\> Get-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly"

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="84a0c-112">取得名為「sampleAssembly」的程式集，該元件位於包含在資源群組 "sampleResourceGroup" 中的整合帳戶 "sampleIntegrationAccount" 中。</span><span class="sxs-lookup"><span data-stu-id="84a0c-112">Get an assembly named "sampleAssembly" located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

### <span data-ttu-id="84a0c-113">範例2：依參數列出整合帳戶中的所有元件</span><span class="sxs-lookup"><span data-stu-id="84a0c-113">Example 2: List all assemblies in an integration account by parameters</span></span>
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

<span data-ttu-id="84a0c-114">取得位於整合帳戶 "sampleIntegrationAccount" 中的所有元件，該集合包含在資源群組 "sampleResourceGroup" 中。</span><span class="sxs-lookup"><span data-stu-id="84a0c-114">Get all assemblies located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

## <span data-ttu-id="84a0c-115">參數</span><span class="sxs-lookup"><span data-stu-id="84a0c-115">PARAMETERS</span></span>

### <span data-ttu-id="84a0c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84a0c-116">-DefaultProfile</span></span>
<span data-ttu-id="84a0c-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="84a0c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84a0c-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="84a0c-118">-Name</span></span>
<span data-ttu-id="84a0c-119">整合帳戶元件名稱。</span><span class="sxs-lookup"><span data-stu-id="84a0c-119">The integration account assembly name.</span></span>

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

### <span data-ttu-id="84a0c-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="84a0c-120">-ParentName</span></span>
<span data-ttu-id="84a0c-121">整合帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="84a0c-121">The integration account name.</span></span>

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

### <span data-ttu-id="84a0c-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="84a0c-122">-ParentObject</span></span>
<span data-ttu-id="84a0c-123">整合帳戶物件。</span><span class="sxs-lookup"><span data-stu-id="84a0c-123">An integration account object.</span></span>

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

### <span data-ttu-id="84a0c-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="84a0c-124">-ParentResourceId</span></span>
<span data-ttu-id="84a0c-125">整合帳戶資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="84a0c-125">The integration account resource id.</span></span>

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

### <span data-ttu-id="84a0c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84a0c-126">-ResourceGroupName</span></span>
<span data-ttu-id="84a0c-127">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="84a0c-127">The resource group name.</span></span>

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

### <span data-ttu-id="84a0c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84a0c-128">CommonParameters</span></span>
<span data-ttu-id="84a0c-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="84a0c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84a0c-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="84a0c-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84a0c-131">輸入</span><span class="sxs-lookup"><span data-stu-id="84a0c-131">INPUTS</span></span>

### <span data-ttu-id="84a0c-132">IntegrationAccount 的管理邏輯。</span><span class="sxs-lookup"><span data-stu-id="84a0c-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="84a0c-133">System.object</span><span class="sxs-lookup"><span data-stu-id="84a0c-133">System.String</span></span>

## <span data-ttu-id="84a0c-134">輸出</span><span class="sxs-lookup"><span data-stu-id="84a0c-134">OUTPUTS</span></span>

### <span data-ttu-id="84a0c-135">PSIntegrationAccountAssembly 中的 LogicApp。</span><span class="sxs-lookup"><span data-stu-id="84a0c-135">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="84a0c-136">筆記</span><span class="sxs-lookup"><span data-stu-id="84a0c-136">NOTES</span></span>

## <span data-ttu-id="84a0c-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="84a0c-137">RELATED LINKS</span></span>