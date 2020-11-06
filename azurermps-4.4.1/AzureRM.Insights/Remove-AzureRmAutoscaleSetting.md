---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 6140E973-D7AB-4A28-A4FA-818E08129372
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAutoscaleSetting.md
ms.openlocfilehash: cd853184e06403f3c0d516ee1b0790c724adacb4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453491"
---
# <span data-ttu-id="58970-101">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="58970-101">Remove-AzureRmAutoscaleSetting</span></span>

## <span data-ttu-id="58970-102">摘要</span><span class="sxs-lookup"><span data-stu-id="58970-102">SYNOPSIS</span></span>
<span data-ttu-id="58970-103">移除自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="58970-103">Removes an Autoscale setting.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58970-104">句法</span><span class="sxs-lookup"><span data-stu-id="58970-104">SYNTAX</span></span>

```
Remove-AzureRmAutoscaleSetting -ResourceGroup <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58970-105">說明</span><span class="sxs-lookup"><span data-stu-id="58970-105">DESCRIPTION</span></span>
<span data-ttu-id="58970-106">**AzureRmAutoscaleSetting** Cmdlet 會移除自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="58970-106">The **Remove-AzureRmAutoscaleSetting** cmdlet removes an Autoscale setting.</span></span>
<span data-ttu-id="58970-107">您必須指定設定的名稱，以及其所指派之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="58970-107">You must specify the name of the setting and the name of the resource group to which it is assigned.</span></span>

## <span data-ttu-id="58970-108">示例</span><span class="sxs-lookup"><span data-stu-id="58970-108">EXAMPLES</span></span>

## <span data-ttu-id="58970-109">參數</span><span class="sxs-lookup"><span data-stu-id="58970-109">PARAMETERS</span></span>

### <span data-ttu-id="58970-110">-名稱</span><span class="sxs-lookup"><span data-stu-id="58970-110">-Name</span></span>
<span data-ttu-id="58970-111">指定要移除的自動縮放設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="58970-111">Specifies the name of the Autoscale setting to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58970-112">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="58970-112">-ResourceGroup</span></span>
<span data-ttu-id="58970-113">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="58970-113">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58970-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58970-114">-DefaultProfile</span></span>
<span data-ttu-id="58970-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="58970-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58970-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58970-116">CommonParameters</span></span>
<span data-ttu-id="58970-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="58970-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58970-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="58970-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58970-119">輸入</span><span class="sxs-lookup"><span data-stu-id="58970-119">INPUTS</span></span>

## <span data-ttu-id="58970-120">輸出</span><span class="sxs-lookup"><span data-stu-id="58970-120">OUTPUTS</span></span>

### <span data-ttu-id="58970-121">AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="58970-121">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="58970-122">筆記</span><span class="sxs-lookup"><span data-stu-id="58970-122">NOTES</span></span>

## <span data-ttu-id="58970-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="58970-123">RELATED LINKS</span></span>

[<span data-ttu-id="58970-124">附加 AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="58970-124">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="58970-125">AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="58970-125">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)


