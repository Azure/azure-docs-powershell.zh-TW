---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: 26a2e414f05fc0aeb209afa946ae168c59ea4ff8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98449067"
---
# <span data-ttu-id="8e985-101">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="8e985-101">Get-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="8e985-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8e985-102">SYNOPSIS</span></span>
<span data-ttu-id="8e985-103">取得整合帳戶批次設定。</span><span class="sxs-lookup"><span data-stu-id="8e985-103">Gets an integration account batch configuration.</span></span>

## <span data-ttu-id="8e985-104">句法</span><span class="sxs-lookup"><span data-stu-id="8e985-104">SYNTAX</span></span>

### <span data-ttu-id="8e985-105">ByIntegrationAccount (預設) </span><span class="sxs-lookup"><span data-stu-id="8e985-105">ByIntegrationAccount (Default)</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e985-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8e985-106">ByInputObject</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e985-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8e985-107">ByResourceId</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e985-108">說明</span><span class="sxs-lookup"><span data-stu-id="8e985-108">DESCRIPTION</span></span>
<span data-ttu-id="8e985-109">**AzIntegrationAccountBatchConfiguration** Cmdlet 會從整合帳戶取得批次設定。</span><span class="sxs-lookup"><span data-stu-id="8e985-109">The **Get-AzIntegrationAccountBatchConfiguration** cmdlet gets an batch configuration from an integration account.</span></span>

## <span data-ttu-id="8e985-110">示例</span><span class="sxs-lookup"><span data-stu-id="8e985-110">EXAMPLES</span></span>

### <span data-ttu-id="8e985-111">範例1：透過參數取得批次設定</span><span class="sxs-lookup"><span data-stu-id="8e985-111">Example 1: Get a batch configuration by parameters</span></span>
```powershell
PS C:\> Get-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="8e985-112">取得名為「sampleBatchConfig」的批次配置，該設定會位於包含在資源群組 "sampleResourceGroup" 的整合帳戶 "sampleIntegrationAccount" 中。</span><span class="sxs-lookup"><span data-stu-id="8e985-112">Get a batch configuration named "sampleBatchConfig" located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

### <span data-ttu-id="8e985-113">範例2：依參數列出整合帳戶中的所有批次設定</span><span class="sxs-lookup"><span data-stu-id="8e985-113">Example 2: List all batch configurations in an integration account by parameters</span></span>
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

<span data-ttu-id="8e985-114">取得位於整合帳戶 "sampleIntegrationAccount" 中的所有批次設定（包含在資源群組 "sampleResourceGroup" 中）。</span><span class="sxs-lookup"><span data-stu-id="8e985-114">Get all batch configurations located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

## <span data-ttu-id="8e985-115">參數</span><span class="sxs-lookup"><span data-stu-id="8e985-115">PARAMETERS</span></span>

### <span data-ttu-id="8e985-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e985-116">-DefaultProfile</span></span>
<span data-ttu-id="8e985-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8e985-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e985-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="8e985-118">-Name</span></span>
<span data-ttu-id="8e985-119">整合帳戶批次配置名稱。</span><span class="sxs-lookup"><span data-stu-id="8e985-119">The integration account batch configuration name.</span></span>

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

### <span data-ttu-id="8e985-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="8e985-120">-ParentName</span></span>
<span data-ttu-id="8e985-121">整合帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="8e985-121">The integration account name.</span></span>

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

### <span data-ttu-id="8e985-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="8e985-122">-ParentObject</span></span>
<span data-ttu-id="8e985-123">整合帳戶物件。</span><span class="sxs-lookup"><span data-stu-id="8e985-123">An integration account object.</span></span>

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

### <span data-ttu-id="8e985-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="8e985-124">-ParentResourceId</span></span>
<span data-ttu-id="8e985-125">整合帳戶資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="8e985-125">The integration account resource id.</span></span>

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

### <span data-ttu-id="8e985-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e985-126">-ResourceGroupName</span></span>
<span data-ttu-id="8e985-127">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8e985-127">The resource group name.</span></span>

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

### <span data-ttu-id="8e985-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e985-128">CommonParameters</span></span>
<span data-ttu-id="8e985-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8e985-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e985-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8e985-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e985-131">輸入</span><span class="sxs-lookup"><span data-stu-id="8e985-131">INPUTS</span></span>

### <span data-ttu-id="8e985-132">IntegrationAccount 的管理邏輯。</span><span class="sxs-lookup"><span data-stu-id="8e985-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="8e985-133">System.object</span><span class="sxs-lookup"><span data-stu-id="8e985-133">System.String</span></span>

## <span data-ttu-id="8e985-134">輸出</span><span class="sxs-lookup"><span data-stu-id="8e985-134">OUTPUTS</span></span>

### <span data-ttu-id="8e985-135">PSIntegrationAccountBatchConfiguration 中的 LogicApp。</span><span class="sxs-lookup"><span data-stu-id="8e985-135">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="8e985-136">筆記</span><span class="sxs-lookup"><span data-stu-id="8e985-136">NOTES</span></span>

## <span data-ttu-id="8e985-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="8e985-137">RELATED LINKS</span></span>
