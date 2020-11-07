---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayavailablewafrulesets
schema: 2.0.0
ms.openlocfilehash: 83ee8e673271079690c24691f22badfe5193ba50
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800902"
---
# <span data-ttu-id="d97af-101">Get-AzureRmApplicationGatewayAvailableWafRuleSets</span><span class="sxs-lookup"><span data-stu-id="d97af-101">Get-AzureRmApplicationGatewayAvailableWafRuleSets</span></span>

## <span data-ttu-id="d97af-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d97af-102">SYNOPSIS</span></span>
<span data-ttu-id="d97af-103">取得所有可用的 web 應用程式防火牆規則集。</span><span class="sxs-lookup"><span data-stu-id="d97af-103">Gets all available web application firewall rule sets.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d97af-104">句法</span><span class="sxs-lookup"><span data-stu-id="d97af-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAvailableWafRuleSets [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d97af-105">說明</span><span class="sxs-lookup"><span data-stu-id="d97af-105">DESCRIPTION</span></span>
<span data-ttu-id="d97af-106">**AzureRmApplicationGatewayAvailableWafRuleSets** Cmdlet 會取得所有可用的 web 應用程式防火牆規則集。</span><span class="sxs-lookup"><span data-stu-id="d97af-106">The **Get-AzureRmApplicationGatewayAvailableWafRuleSets** cmdlet gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="d97af-107">示例</span><span class="sxs-lookup"><span data-stu-id="d97af-107">EXAMPLES</span></span>

### <span data-ttu-id="d97af-108">範例1</span><span class="sxs-lookup"><span data-stu-id="d97af-108">Example 1</span></span>
```
PS C:\>$availableRuleSets = Get-AzureRmApplicationGatewayAvailableWafRuleSets
```

<span data-ttu-id="d97af-109">這個命令會傳回所有可用的 web 應用程式防火牆規則集。</span><span class="sxs-lookup"><span data-stu-id="d97af-109">This commands returns all the available web application firewall rule sets.</span></span>

## <span data-ttu-id="d97af-110">參數</span><span class="sxs-lookup"><span data-stu-id="d97af-110">PARAMETERS</span></span>

### <span data-ttu-id="d97af-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d97af-111">-DefaultProfile</span></span>
<span data-ttu-id="d97af-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d97af-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d97af-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d97af-113">CommonParameters</span></span>
<span data-ttu-id="d97af-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d97af-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d97af-115">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d97af-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d97af-116">輸入</span><span class="sxs-lookup"><span data-stu-id="d97af-116">INPUTS</span></span>

### <span data-ttu-id="d97af-117">所有</span><span class="sxs-lookup"><span data-stu-id="d97af-117">None</span></span>

## <span data-ttu-id="d97af-118">輸出</span><span class="sxs-lookup"><span data-stu-id="d97af-118">OUTPUTS</span></span>

### <span data-ttu-id="d97af-119">PSApplicationGatewayAvailableWafRuleSetsResult 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d97af-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span></span>

## <span data-ttu-id="d97af-120">筆記</span><span class="sxs-lookup"><span data-stu-id="d97af-120">NOTES</span></span>
<span data-ttu-id="d97af-121">**清單-AzureRmApplicationGatewayAvailableWafRuleSets** 是 **AzureRmApplicationGatewayAvailableWafRuleSets** Cmdlet 的別名。</span><span class="sxs-lookup"><span data-stu-id="d97af-121">**List-AzureRmApplicationGatewayAvailableWafRuleSets** is an alias for the **Get-AzureRmApplicationGatewayAvailableWafRuleSets** cmdlet.</span></span>

## <span data-ttu-id="d97af-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="d97af-122">RELATED LINKS</span></span>

