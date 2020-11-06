---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/get-azadvisorconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorConfiguration.md
ms.openlocfilehash: d17384b47e4a722631b5d3003bdb4b7eb430836d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614156"
---
# <span data-ttu-id="b7ae8-101">Get-AzAdvisorConfiguration</span><span class="sxs-lookup"><span data-stu-id="b7ae8-101">Get-AzAdvisorConfiguration</span></span>

## <span data-ttu-id="b7ae8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b7ae8-102">SYNOPSIS</span></span>
<span data-ttu-id="b7ae8-103">取得指定訂閱或資源群組的 Azure Advisor 設定。</span><span class="sxs-lookup"><span data-stu-id="b7ae8-103">Get the Azure Advisor configurations for the given subscription or resource group.</span></span>

## <span data-ttu-id="b7ae8-104">句法</span><span class="sxs-lookup"><span data-stu-id="b7ae8-104">SYNTAX</span></span>

```
Get-AzAdvisorConfiguration [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b7ae8-105">說明</span><span class="sxs-lookup"><span data-stu-id="b7ae8-105">DESCRIPTION</span></span>
<span data-ttu-id="b7ae8-106">與訂閱相關聯的配置有兩種類型：</span><span class="sxs-lookup"><span data-stu-id="b7ae8-106">The configurations associated with a subscription have two types:</span></span>

<span data-ttu-id="b7ae8-107">訂閱階層配置：訂閱只能有一個此類型的設定。</span><span class="sxs-lookup"><span data-stu-id="b7ae8-107">Subscription level configuration: There can be only one configuration of this type for a subscription.</span></span> <span data-ttu-id="b7ae8-108">LowCpuThreshold 和 Exclude 是此類型設定的唯一屬性。</span><span class="sxs-lookup"><span data-stu-id="b7ae8-108">LowCpuThreshold and Exclude are the only property of this type of configuration.</span></span>

<span data-ttu-id="b7ae8-109">ResourceGroup 層次配置：訂閱中的每個 ResourceGroup 只能有一個設定。</span><span class="sxs-lookup"><span data-stu-id="b7ae8-109">ResourceGroup level configuration: There can be only one configuration for each ResourceGroup in a subscription.</span></span> <span data-ttu-id="b7ae8-110">[排除] 是此類型設定的唯一屬性。</span><span class="sxs-lookup"><span data-stu-id="b7ae8-110">Exclude is the only property of this type of configuration.</span></span>

## <span data-ttu-id="b7ae8-111">示例</span><span class="sxs-lookup"><span data-stu-id="b7ae8-111">EXAMPLES</span></span>

### <span data-ttu-id="b7ae8-112">範例1</span><span class="sxs-lookup"><span data-stu-id="b7ae8-112">Example 1</span></span>
```powershell
PS C:\>$data = Get-AzAdvisorConfiguration
Id         : /subscriptions/{user_subscription}/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationProperties
Type       : Microsoft.Advisor/Configurations

Id         : /subscriptions/{user_subscription}/providers/Microsoft.Advisor/configurations/{user_subscription}-{resourceGroupName}
Name       : {user_subscription}-{resourceGroupName}
Properties : Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationProperties
Type       : Microsoft.Advisor/Configurations

PS C:\>$data[0].Properties
AdditionalProperties :
Exclude              : False
LowCpuThreshold      : 20

PS C:\>$data[1].Properties
AdditionalProperties :
Exclude              : True
LowCpuThreshold      : null

```
<span data-ttu-id="b7ae8-113">檢索 Azure Advisor 配置 (s 的清單) 。</span><span class="sxs-lookup"><span data-stu-id="b7ae8-113">Retrieves a list of Azure Advisor Configuration(s).</span></span>

## <span data-ttu-id="b7ae8-114">參數</span><span class="sxs-lookup"><span data-stu-id="b7ae8-114">PARAMETERS</span></span>

### <span data-ttu-id="b7ae8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7ae8-115">-DefaultProfile</span></span>
<span data-ttu-id="b7ae8-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b7ae8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7ae8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7ae8-117">-ResourceGroupName</span></span>
<span data-ttu-id="b7ae8-118">配置的資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="b7ae8-118">Resource Group name of the configuration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7ae8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7ae8-119">CommonParameters</span></span>
<span data-ttu-id="b7ae8-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b7ae8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b7ae8-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b7ae8-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7ae8-122">輸入</span><span class="sxs-lookup"><span data-stu-id="b7ae8-122">INPUTS</span></span>

### <span data-ttu-id="b7ae8-123">所有</span><span class="sxs-lookup"><span data-stu-id="b7ae8-123">None</span></span>

## <span data-ttu-id="b7ae8-124">輸出</span><span class="sxs-lookup"><span data-stu-id="b7ae8-124">OUTPUTS</span></span>

### <span data-ttu-id="b7ae8-125">PsAzureAdvisorConfigurationData 中的 [...]</span><span class="sxs-lookup"><span data-stu-id="b7ae8-125">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span></span>

## <span data-ttu-id="b7ae8-126">筆記</span><span class="sxs-lookup"><span data-stu-id="b7ae8-126">NOTES</span></span>

## <span data-ttu-id="b7ae8-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="b7ae8-127">RELATED LINKS</span></span>