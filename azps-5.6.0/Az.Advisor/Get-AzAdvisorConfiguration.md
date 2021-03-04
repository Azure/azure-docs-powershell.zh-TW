---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/powershell/module/az.advisor/get-azadvisorconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorConfiguration.md
ms.openlocfilehash: dd5ca513c327a1ed5d045c3b0283a8b220f6a062
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905678"
---
# <span data-ttu-id="7b85f-101">Get-AzAdvisorConfiguration</span><span class="sxs-lookup"><span data-stu-id="7b85f-101">Get-AzAdvisorConfiguration</span></span>

## <span data-ttu-id="7b85f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7b85f-102">SYNOPSIS</span></span>
<span data-ttu-id="7b85f-103">取得給定訂閱或資源群組的 Azure 建議程式組。</span><span class="sxs-lookup"><span data-stu-id="7b85f-103">Get the Azure Advisor configurations for the given subscription or resource group.</span></span>

## <span data-ttu-id="7b85f-104">語法</span><span class="sxs-lookup"><span data-stu-id="7b85f-104">SYNTAX</span></span>

```
Get-AzAdvisorConfiguration [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7b85f-105">描述</span><span class="sxs-lookup"><span data-stu-id="7b85f-105">DESCRIPTION</span></span>
<span data-ttu-id="7b85f-106">與訂閱相關聯的組配置有兩種類型：</span><span class="sxs-lookup"><span data-stu-id="7b85f-106">The configurations associated with a subscription have two types:</span></span>

<span data-ttu-id="7b85f-107">訂閱層級組式：訂閱只能有一種這種類型的組式。</span><span class="sxs-lookup"><span data-stu-id="7b85f-107">Subscription level configuration: There can be only one configuration of this type for a subscription.</span></span> <span data-ttu-id="7b85f-108">Low 是否擁有和排除是此類型組式的唯一屬性。</span><span class="sxs-lookup"><span data-stu-id="7b85f-108">LowCpuThreshold and Exclude are the only property of this type of configuration.</span></span>

<span data-ttu-id="7b85f-109">ResourceGroup 層級組配置：訂閱中每個 ResourceGroup 只能有一個組組。</span><span class="sxs-lookup"><span data-stu-id="7b85f-109">ResourceGroup level configuration: There can be only one configuration for each ResourceGroup in a subscription.</span></span> <span data-ttu-id="7b85f-110">排除是此類型組式的唯一屬性。</span><span class="sxs-lookup"><span data-stu-id="7b85f-110">Exclude is the only property of this type of configuration.</span></span>

## <span data-ttu-id="7b85f-111">例子</span><span class="sxs-lookup"><span data-stu-id="7b85f-111">EXAMPLES</span></span>

### <span data-ttu-id="7b85f-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="7b85f-112">Example 1</span></span>
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
<span data-ttu-id="7b85f-113">會從清單中 (Azure 建議) 。</span><span class="sxs-lookup"><span data-stu-id="7b85f-113">Retrieves a list of Azure Advisor Configuration(s).</span></span>

## <span data-ttu-id="7b85f-114">參數</span><span class="sxs-lookup"><span data-stu-id="7b85f-114">PARAMETERS</span></span>

### <span data-ttu-id="7b85f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b85f-115">-DefaultProfile</span></span>
<span data-ttu-id="7b85f-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7b85f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b85f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b85f-117">-ResourceGroupName</span></span>
<span data-ttu-id="7b85f-118">組配置的資源組名</span><span class="sxs-lookup"><span data-stu-id="7b85f-118">Resource Group name of the configuration</span></span>

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

### <span data-ttu-id="7b85f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b85f-119">CommonParameters</span></span>
<span data-ttu-id="7b85f-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7b85f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="7b85f-121">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="7b85f-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b85f-122">輸入</span><span class="sxs-lookup"><span data-stu-id="7b85f-122">INPUTS</span></span>

### <span data-ttu-id="7b85f-123">沒有</span><span class="sxs-lookup"><span data-stu-id="7b85f-123">None</span></span>

## <span data-ttu-id="7b85f-124">輸出</span><span class="sxs-lookup"><span data-stu-id="7b85f-124">OUTPUTS</span></span>

### <span data-ttu-id="7b85f-125">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span><span class="sxs-lookup"><span data-stu-id="7b85f-125">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span></span>

## <span data-ttu-id="7b85f-126">筆記</span><span class="sxs-lookup"><span data-stu-id="7b85f-126">NOTES</span></span>

## <span data-ttu-id="7b85f-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="7b85f-127">RELATED LINKS</span></span>
