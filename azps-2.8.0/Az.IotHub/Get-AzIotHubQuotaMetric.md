---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubquotametric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
ms.openlocfilehash: 6d8ea34de1520326ead270ffa44837388729bc5a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612212"
---
# <span data-ttu-id="83f0b-101">Get-AzIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="83f0b-101">Get-AzIotHubQuotaMetric</span></span>

## <span data-ttu-id="83f0b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="83f0b-102">SYNOPSIS</span></span>
<span data-ttu-id="83f0b-103">取得 IotHub 的配額度量單位。</span><span class="sxs-lookup"><span data-stu-id="83f0b-103">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="83f0b-104">句法</span><span class="sxs-lookup"><span data-stu-id="83f0b-104">SYNTAX</span></span>

```
Get-AzIotHubQuotaMetric [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83f0b-105">說明</span><span class="sxs-lookup"><span data-stu-id="83f0b-105">DESCRIPTION</span></span>
<span data-ttu-id="83f0b-106">取得 IotHub 的配額度量單位。</span><span class="sxs-lookup"><span data-stu-id="83f0b-106">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="83f0b-107">示例</span><span class="sxs-lookup"><span data-stu-id="83f0b-107">EXAMPLES</span></span>

### <span data-ttu-id="83f0b-108">範例1取得配額度量單位</span><span class="sxs-lookup"><span data-stu-id="83f0b-108">Example 1 Get the Quota Metrics</span></span>
```
PS C:\> Get-AzIotHubQuotaMetric -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="83f0b-109">取得名為 "myiothub" 的 IotHub 的配額度量資訊</span><span class="sxs-lookup"><span data-stu-id="83f0b-109">Gets the Quota Metric information for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="83f0b-110">參數</span><span class="sxs-lookup"><span data-stu-id="83f0b-110">PARAMETERS</span></span>

### <span data-ttu-id="83f0b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83f0b-111">-DefaultProfile</span></span>
<span data-ttu-id="83f0b-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="83f0b-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="83f0b-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="83f0b-113">-Name</span></span>
<span data-ttu-id="83f0b-114">IoT 中樞的名稱。</span><span class="sxs-lookup"><span data-stu-id="83f0b-114">Name of the IoT hub.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83f0b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83f0b-115">-ResourceGroupName</span></span>
<span data-ttu-id="83f0b-116">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="83f0b-116">Resource Group Name</span></span>

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

### <span data-ttu-id="83f0b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83f0b-117">CommonParameters</span></span>
<span data-ttu-id="83f0b-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="83f0b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83f0b-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="83f0b-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83f0b-120">輸入</span><span class="sxs-lookup"><span data-stu-id="83f0b-120">INPUTS</span></span>

### <span data-ttu-id="83f0b-121">System.object</span><span class="sxs-lookup"><span data-stu-id="83f0b-121">System.String</span></span>

## <span data-ttu-id="83f0b-122">輸出</span><span class="sxs-lookup"><span data-stu-id="83f0b-122">OUTPUTS</span></span>

### <span data-ttu-id="83f0b-123">PSIotHubQuotaMetric （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="83f0b-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubQuotaMetric</span></span>

## <span data-ttu-id="83f0b-124">筆記</span><span class="sxs-lookup"><span data-stu-id="83f0b-124">NOTES</span></span>

## <span data-ttu-id="83f0b-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="83f0b-125">RELATED LINKS</span></span>
