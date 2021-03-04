---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: 722f2bd79230de11c12ab0448fb39ed3ad49f00d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904098"
---
# <span data-ttu-id="7b2a3-101">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="7b2a3-101">Get-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="7b2a3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7b2a3-102">SYNOPSIS</span></span>
<span data-ttu-id="7b2a3-103">獲得整合帳戶批次組組。</span><span class="sxs-lookup"><span data-stu-id="7b2a3-103">Gets an integration account batch configuration.</span></span>

## <span data-ttu-id="7b2a3-104">語法</span><span class="sxs-lookup"><span data-stu-id="7b2a3-104">SYNTAX</span></span>

### <span data-ttu-id="7b2a3-105">By方Account (預設) </span><span class="sxs-lookup"><span data-stu-id="7b2a3-105">ByIntegrationAccount (Default)</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b2a3-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7b2a3-106">ByInputObject</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b2a3-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7b2a3-107">ByResourceId</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b2a3-108">描述</span><span class="sxs-lookup"><span data-stu-id="7b2a3-108">DESCRIPTION</span></span>
<span data-ttu-id="7b2a3-109">**Get-Az有AccountBatchConfiguration** Cmdlet 會從整合帳戶取得批次組配置。</span><span class="sxs-lookup"><span data-stu-id="7b2a3-109">The **Get-AzIntegrationAccountBatchConfiguration** cmdlet gets an batch configuration from an integration account.</span></span>

## <span data-ttu-id="7b2a3-110">例子</span><span class="sxs-lookup"><span data-stu-id="7b2a3-110">EXAMPLES</span></span>

### <span data-ttu-id="7b2a3-111">範例 1：根據參數取得批次設定</span><span class="sxs-lookup"><span data-stu-id="7b2a3-111">Example 1: Get a batch configuration by parameters</span></span>
```powershell
PS C:\> Get-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="7b2a3-112">取得名為"sampleBatchConfig"的批次組組，該組組位於整合帳戶"sampleSourceAccount"中，該群組包含在資源群組"sampleResourceGroup"中。</span><span class="sxs-lookup"><span data-stu-id="7b2a3-112">Get a batch configuration named "sampleBatchConfig" located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

### <span data-ttu-id="7b2a3-113">範例 2：以參數列出整合帳戶中的所有批次設定</span><span class="sxs-lookup"><span data-stu-id="7b2a3-113">Example 2: List all batch configurations in an integration account by parameters</span></span>
```powershell
PS C:\> Get-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig2
Name       : sampleBatchConfig2
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="7b2a3-114">取得位於整合帳戶 "sample準備Account"的所有批次組式組，此帳戶包含在資源群組"sampleResourceGroup"中。</span><span class="sxs-lookup"><span data-stu-id="7b2a3-114">Get all batch configurations located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

## <span data-ttu-id="7b2a3-115">參數</span><span class="sxs-lookup"><span data-stu-id="7b2a3-115">PARAMETERS</span></span>

### <span data-ttu-id="7b2a3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b2a3-116">-DefaultProfile</span></span>
<span data-ttu-id="7b2a3-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7b2a3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b2a3-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="7b2a3-118">-Name</span></span>
<span data-ttu-id="7b2a3-119">整合帳戶批次組組名稱。</span><span class="sxs-lookup"><span data-stu-id="7b2a3-119">The integration account batch configuration name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BatchConfigurationName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b2a3-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="7b2a3-120">-ParentName</span></span>
<span data-ttu-id="7b2a3-121">整合帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="7b2a3-121">The integration account name.</span></span>

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

### <span data-ttu-id="7b2a3-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="7b2a3-122">-ParentObject</span></span>
<span data-ttu-id="7b2a3-123">整合帳戶物件。</span><span class="sxs-lookup"><span data-stu-id="7b2a3-123">An integration account object.</span></span>

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

### <span data-ttu-id="7b2a3-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="7b2a3-124">-ParentResourceId</span></span>
<span data-ttu-id="7b2a3-125">整合帳戶資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="7b2a3-125">The integration account resource id.</span></span>

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

### <span data-ttu-id="7b2a3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b2a3-126">-ResourceGroupName</span></span>
<span data-ttu-id="7b2a3-127">資源組名。</span><span class="sxs-lookup"><span data-stu-id="7b2a3-127">The resource group name.</span></span>

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

### <span data-ttu-id="7b2a3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b2a3-128">CommonParameters</span></span>
<span data-ttu-id="7b2a3-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7b2a3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b2a3-130">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="7b2a3-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b2a3-131">輸入</span><span class="sxs-lookup"><span data-stu-id="7b2a3-131">INPUTS</span></span>

### <span data-ttu-id="7b2a3-132">Microsoft.Azure.management.Logic.models.IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="7b2a3-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="7b2a3-133">System.String</span><span class="sxs-lookup"><span data-stu-id="7b2a3-133">System.String</span></span>

## <span data-ttu-id="7b2a3-134">輸出</span><span class="sxs-lookup"><span data-stu-id="7b2a3-134">OUTPUTS</span></span>

### <span data-ttu-id="7b2a3-135">Microsoft.Azure.Commands.LogicApp.models.PS方AccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="7b2a3-135">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="7b2a3-136">筆記</span><span class="sxs-lookup"><span data-stu-id="7b2a3-136">NOTES</span></span>

## <span data-ttu-id="7b2a3-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="7b2a3-137">RELATED LINKS</span></span>
