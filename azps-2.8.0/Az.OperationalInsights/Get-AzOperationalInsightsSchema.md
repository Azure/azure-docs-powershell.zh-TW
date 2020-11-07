---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 6A834F26-C3D1-46DA-A4A6-1BB5B69291D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSchema.md
ms.openlocfilehash: 077272f15d37645de86f144424fddd7e5f026908
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2020
ms.locfileid: "93799422"
---
# <span data-ttu-id="c2b8a-101">Get-AzOperationalInsightsSchema</span><span class="sxs-lookup"><span data-stu-id="c2b8a-101">Get-AzOperationalInsightsSchema</span></span>

## <span data-ttu-id="c2b8a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c2b8a-102">SYNOPSIS</span></span>
<span data-ttu-id="c2b8a-103">傳回與工作區相關聯的架構。</span><span class="sxs-lookup"><span data-stu-id="c2b8a-103">Returns the schema associated with a workspace.</span></span>

## <span data-ttu-id="c2b8a-104">句法</span><span class="sxs-lookup"><span data-stu-id="c2b8a-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsSchema [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2b8a-105">說明</span><span class="sxs-lookup"><span data-stu-id="c2b8a-105">DESCRIPTION</span></span>
<span data-ttu-id="c2b8a-106">**AzOperationalInsightsSchema** Cmdlet 會傳回與該資源群組中指定的工作區相關聯的架構。</span><span class="sxs-lookup"><span data-stu-id="c2b8a-106">The **Get-AzOperationalInsightsSchema** cmdlet returns the schema associated with the specified workspace within that resource group.</span></span>

## <span data-ttu-id="c2b8a-107">示例</span><span class="sxs-lookup"><span data-stu-id="c2b8a-107">EXAMPLES</span></span>

### <span data-ttu-id="c2b8a-108">範例1：取得工作區的架構</span><span class="sxs-lookup"><span data-stu-id="c2b8a-108">Example 1: Get the schemas for a workspace</span></span>
```
PS C:\>Get-AzOperationalInsightsSchema -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="c2b8a-109">這個命令會取得與工作區相關聯的架構。</span><span class="sxs-lookup"><span data-stu-id="c2b8a-109">This command gets the schemas associated with a workspace.</span></span>

## <span data-ttu-id="c2b8a-110">參數</span><span class="sxs-lookup"><span data-stu-id="c2b8a-110">PARAMETERS</span></span>

### <span data-ttu-id="c2b8a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2b8a-111">-DefaultProfile</span></span>
<span data-ttu-id="c2b8a-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="c2b8a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c2b8a-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2b8a-113">-ResourceGroupName</span></span>
<span data-ttu-id="c2b8a-114">指定包含工作區之 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c2b8a-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="c2b8a-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c2b8a-115">-WorkspaceName</span></span>
<span data-ttu-id="c2b8a-116">指定工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="c2b8a-116">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="c2b8a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2b8a-117">CommonParameters</span></span>
<span data-ttu-id="c2b8a-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c2b8a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2b8a-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c2b8a-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2b8a-120">輸入</span><span class="sxs-lookup"><span data-stu-id="c2b8a-120">INPUTS</span></span>

### <span data-ttu-id="c2b8a-121">System.object</span><span class="sxs-lookup"><span data-stu-id="c2b8a-121">System.String</span></span>

## <span data-ttu-id="c2b8a-122">輸出</span><span class="sxs-lookup"><span data-stu-id="c2b8a-122">OUTPUTS</span></span>

### <span data-ttu-id="c2b8a-123">PSSearchGetSchemaResponse 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="c2b8a-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSchemaResponse</span></span>

## <span data-ttu-id="c2b8a-124">筆記</span><span class="sxs-lookup"><span data-stu-id="c2b8a-124">NOTES</span></span>

## <span data-ttu-id="c2b8a-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="c2b8a-125">RELATED LINKS</span></span>

[<span data-ttu-id="c2b8a-126">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c2b8a-126">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


