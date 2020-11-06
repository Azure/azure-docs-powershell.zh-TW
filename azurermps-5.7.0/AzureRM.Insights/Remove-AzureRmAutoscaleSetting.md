---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 6140E973-D7AB-4A28-A4FA-818E08129372
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermautoscalesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAutoscaleSetting.md
ms.openlocfilehash: 4d6c2f748915847038ef4029dc024763375ef99e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447804"
---
# <span data-ttu-id="8d8ec-101">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="8d8ec-101">Remove-AzureRmAutoscaleSetting</span></span>

## <span data-ttu-id="8d8ec-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8d8ec-102">SYNOPSIS</span></span>
<span data-ttu-id="8d8ec-103">移除自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="8d8ec-103">Removes an Autoscale setting.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d8ec-104">句法</span><span class="sxs-lookup"><span data-stu-id="8d8ec-104">SYNTAX</span></span>

```
Remove-AzureRmAutoscaleSetting -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d8ec-105">說明</span><span class="sxs-lookup"><span data-stu-id="8d8ec-105">DESCRIPTION</span></span>
<span data-ttu-id="8d8ec-106">**AzureRmAutoscaleSetting** Cmdlet 會移除自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="8d8ec-106">The **Remove-AzureRmAutoscaleSetting** cmdlet removes an Autoscale setting.</span></span>
<span data-ttu-id="8d8ec-107">您必須指定設定的名稱，以及其所指派之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8d8ec-107">You must specify the name of the setting and the name of the resource group to which it is assigned.</span></span>

<span data-ttu-id="8d8ec-108">這個 Cmdlet 會實現 ShouldProcess 模式，亦即，在實際建立、修改或移除資源之前，它可能會要求使用者進行確認。</span><span class="sxs-lookup"><span data-stu-id="8d8ec-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="8d8ec-109">示例</span><span class="sxs-lookup"><span data-stu-id="8d8ec-109">EXAMPLES</span></span>

## <span data-ttu-id="8d8ec-110">參數</span><span class="sxs-lookup"><span data-stu-id="8d8ec-110">PARAMETERS</span></span>

### <span data-ttu-id="8d8ec-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d8ec-111">-DefaultProfile</span></span>
<span data-ttu-id="8d8ec-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="8d8ec-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8d8ec-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="8d8ec-113">-Name</span></span>
<span data-ttu-id="8d8ec-114">指定要移除的自動縮放設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="8d8ec-114">Specifies the name of the Autoscale setting to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d8ec-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d8ec-115">-ResourceGroupName</span></span>
<span data-ttu-id="8d8ec-116">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8d8ec-116">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d8ec-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d8ec-117">CommonParameters</span></span>
<span data-ttu-id="8d8ec-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8d8ec-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d8ec-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8d8ec-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d8ec-120">輸入</span><span class="sxs-lookup"><span data-stu-id="8d8ec-120">INPUTS</span></span>

### <span data-ttu-id="8d8ec-121">所有</span><span class="sxs-lookup"><span data-stu-id="8d8ec-121">None</span></span>
<span data-ttu-id="8d8ec-122">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="8d8ec-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8d8ec-123">輸出</span><span class="sxs-lookup"><span data-stu-id="8d8ec-123">OUTPUTS</span></span>

### <span data-ttu-id="8d8ec-124">AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="8d8ec-124">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="8d8ec-125">筆記</span><span class="sxs-lookup"><span data-stu-id="8d8ec-125">NOTES</span></span>

## <span data-ttu-id="8d8ec-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="8d8ec-126">RELATED LINKS</span></span>

[<span data-ttu-id="8d8ec-127">附加 AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="8d8ec-127">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="8d8ec-128">AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="8d8ec-128">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)


