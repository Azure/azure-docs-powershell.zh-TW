---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubquotametric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
ms.openlocfilehash: 7da36f401647a4e020097eb2cfe6690aa1327755
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794712"
---
# <span data-ttu-id="13027-101">Get-AzIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="13027-101">Get-AzIotHubQuotaMetric</span></span>

## <span data-ttu-id="13027-102">摘要</span><span class="sxs-lookup"><span data-stu-id="13027-102">SYNOPSIS</span></span>
<span data-ttu-id="13027-103">取得 IotHub 的配額度量單位。</span><span class="sxs-lookup"><span data-stu-id="13027-103">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="13027-104">句法</span><span class="sxs-lookup"><span data-stu-id="13027-104">SYNTAX</span></span>

```
Get-AzIotHubQuotaMetric [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13027-105">說明</span><span class="sxs-lookup"><span data-stu-id="13027-105">DESCRIPTION</span></span>
<span data-ttu-id="13027-106">取得 IotHub 的配額度量單位。</span><span class="sxs-lookup"><span data-stu-id="13027-106">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="13027-107">示例</span><span class="sxs-lookup"><span data-stu-id="13027-107">EXAMPLES</span></span>

### <span data-ttu-id="13027-108">範例1取得配額度量單位</span><span class="sxs-lookup"><span data-stu-id="13027-108">Example 1 Get the Quota Metrics</span></span>
```
PS C:\> Get-AzIotHubQuotaMetric -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="13027-109">取得名為 "myiothub" 的 IotHub 的配額度量資訊</span><span class="sxs-lookup"><span data-stu-id="13027-109">Gets the Quota Metric information for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="13027-110">參數</span><span class="sxs-lookup"><span data-stu-id="13027-110">PARAMETERS</span></span>

### <span data-ttu-id="13027-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13027-111">-DefaultProfile</span></span>
<span data-ttu-id="13027-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="13027-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="13027-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="13027-113">-Name</span></span>
<span data-ttu-id="13027-114">IoT 中樞的名稱。</span><span class="sxs-lookup"><span data-stu-id="13027-114">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="13027-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13027-115">-ResourceGroupName</span></span>
<span data-ttu-id="13027-116">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="13027-116">Resource Group Name</span></span>

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

### <span data-ttu-id="13027-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13027-117">CommonParameters</span></span>
<span data-ttu-id="13027-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="13027-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13027-119">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="13027-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13027-120">輸入</span><span class="sxs-lookup"><span data-stu-id="13027-120">INPUTS</span></span>

### <span data-ttu-id="13027-121">System.object</span><span class="sxs-lookup"><span data-stu-id="13027-121">System.String</span></span>

## <span data-ttu-id="13027-122">輸出</span><span class="sxs-lookup"><span data-stu-id="13027-122">OUTPUTS</span></span>

### <span data-ttu-id="13027-123">PSIotHubQuotaMetric （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="13027-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubQuotaMetric</span></span>

## <span data-ttu-id="13027-124">筆記</span><span class="sxs-lookup"><span data-stu-id="13027-124">NOTES</span></span>

## <span data-ttu-id="13027-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="13027-125">RELATED LINKS</span></span>
