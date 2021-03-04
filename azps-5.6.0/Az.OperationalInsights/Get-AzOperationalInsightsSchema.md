---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 6A834F26-C3D1-46DA-A4A6-1BB5B69291D0
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightsschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSchema.md
ms.openlocfilehash: 7f177b94b851f1a3702a153032c715f81badbcc3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916511"
---
# <span data-ttu-id="1bfa7-101">Get-AzOperationalInsightsSchema</span><span class="sxs-lookup"><span data-stu-id="1bfa7-101">Get-AzOperationalInsightsSchema</span></span>

## <span data-ttu-id="1bfa7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1bfa7-102">SYNOPSIS</span></span>
<span data-ttu-id="1bfa7-103">會返回與工作區相關聯的架構。</span><span class="sxs-lookup"><span data-stu-id="1bfa7-103">Returns the schema associated with a workspace.</span></span>

## <span data-ttu-id="1bfa7-104">語法</span><span class="sxs-lookup"><span data-stu-id="1bfa7-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsSchema [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1bfa7-105">描述</span><span class="sxs-lookup"><span data-stu-id="1bfa7-105">DESCRIPTION</span></span>
<span data-ttu-id="1bfa7-106">**Get-AzOperationalInsightsSchdlet** 會返回與該資源群組中指定工作區相關聯的架構。</span><span class="sxs-lookup"><span data-stu-id="1bfa7-106">The **Get-AzOperationalInsightsSchema** cmdlet returns the schema associated with the specified workspace within that resource group.</span></span>

## <span data-ttu-id="1bfa7-107">例子</span><span class="sxs-lookup"><span data-stu-id="1bfa7-107">EXAMPLES</span></span>

### <span data-ttu-id="1bfa7-108">範例 1：取得工作區的架構</span><span class="sxs-lookup"><span data-stu-id="1bfa7-108">Example 1: Get the schemas for a workspace</span></span>
```
PS C:\>Get-AzOperationalInsightsSchema -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="1bfa7-109">此命令會獲得與工作區相關聯的架構。</span><span class="sxs-lookup"><span data-stu-id="1bfa7-109">This command gets the schemas associated with a workspace.</span></span>

## <span data-ttu-id="1bfa7-110">參數</span><span class="sxs-lookup"><span data-stu-id="1bfa7-110">PARAMETERS</span></span>

### <span data-ttu-id="1bfa7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bfa7-111">-DefaultProfile</span></span>
<span data-ttu-id="1bfa7-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="1bfa7-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1bfa7-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bfa7-113">-ResourceGroupName</span></span>
<span data-ttu-id="1bfa7-114">指定包含工作區的 Azure 資源組名。</span><span class="sxs-lookup"><span data-stu-id="1bfa7-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bfa7-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1bfa7-115">-WorkspaceName</span></span>
<span data-ttu-id="1bfa7-116">指定工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="1bfa7-116">Specifies a workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bfa7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bfa7-117">CommonParameters</span></span>
<span data-ttu-id="1bfa7-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1bfa7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bfa7-119">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="1bfa7-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bfa7-120">輸入</span><span class="sxs-lookup"><span data-stu-id="1bfa7-120">INPUTS</span></span>

### <span data-ttu-id="1bfa7-121">System.String</span><span class="sxs-lookup"><span data-stu-id="1bfa7-121">System.String</span></span>

## <span data-ttu-id="1bfa7-122">輸出</span><span class="sxs-lookup"><span data-stu-id="1bfa7-122">OUTPUTS</span></span>

### <span data-ttu-id="1bfa7-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSchemaResponse</span><span class="sxs-lookup"><span data-stu-id="1bfa7-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSchemaResponse</span></span>

## <span data-ttu-id="1bfa7-124">筆記</span><span class="sxs-lookup"><span data-stu-id="1bfa7-124">NOTES</span></span>

## <span data-ttu-id="1bfa7-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="1bfa7-125">RELATED LINKS</span></span>

[<span data-ttu-id="1bfa7-126">Azure 營運深入資訊 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1bfa7-126">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


