---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/get-azservicebusoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusOperation.md
ms.openlocfilehash: 85dd98ac4eeb262564dcca58ec57f1f5df80842a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912594"
---
# <span data-ttu-id="468ec-101">Get-AzServiceBusOperation</span><span class="sxs-lookup"><span data-stu-id="468ec-101">Get-AzServiceBusOperation</span></span>

## <span data-ttu-id="468ec-102">簡介</span><span class="sxs-lookup"><span data-stu-id="468ec-102">SYNOPSIS</span></span>
<span data-ttu-id="468ec-103">清單支援的 ServiceBus Operations</span><span class="sxs-lookup"><span data-stu-id="468ec-103">List supported ServiceBus Operations</span></span>

## <span data-ttu-id="468ec-104">語法</span><span class="sxs-lookup"><span data-stu-id="468ec-104">SYNTAX</span></span>

```
Get-AzServiceBusOperation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="468ec-105">描述</span><span class="sxs-lookup"><span data-stu-id="468ec-105">DESCRIPTION</span></span>
<span data-ttu-id="468ec-106">**Get-AzServiceBusOperation Cmdlet** 會列出 ServiceBus 支援的作業。</span><span class="sxs-lookup"><span data-stu-id="468ec-106">The **Get-AzServiceBusOperation** cmdlet Lists the ServiceBus supported Operations.</span></span>

## <span data-ttu-id="468ec-107">例子</span><span class="sxs-lookup"><span data-stu-id="468ec-107">EXAMPLES</span></span>

### <span data-ttu-id="468ec-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="468ec-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusOperation
```

<span data-ttu-id="468ec-109">列出 ServiceBus 支援的作業</span><span class="sxs-lookup"><span data-stu-id="468ec-109">Lists ServiceBus supported operations</span></span>

## <span data-ttu-id="468ec-110">參數</span><span class="sxs-lookup"><span data-stu-id="468ec-110">PARAMETERS</span></span>

### <span data-ttu-id="468ec-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="468ec-111">-DefaultProfile</span></span>
<span data-ttu-id="468ec-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="468ec-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="468ec-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="468ec-113">CommonParameters</span></span>
<span data-ttu-id="468ec-114">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="468ec-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="468ec-115">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="468ec-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="468ec-116">輸入</span><span class="sxs-lookup"><span data-stu-id="468ec-116">INPUTS</span></span>

### <span data-ttu-id="468ec-117">沒有</span><span class="sxs-lookup"><span data-stu-id="468ec-117">None</span></span>

## <span data-ttu-id="468ec-118">輸出</span><span class="sxs-lookup"><span data-stu-id="468ec-118">OUTPUTS</span></span>

### <span data-ttu-id="468ec-119">Microsoft.Azure.Commands.ServiceBus.models.PSOperationAttributes</span><span class="sxs-lookup"><span data-stu-id="468ec-119">Microsoft.Azure.Commands.ServiceBus.Models.PSOperationAttributes</span></span>

## <span data-ttu-id="468ec-120">筆記</span><span class="sxs-lookup"><span data-stu-id="468ec-120">NOTES</span></span>

## <span data-ttu-id="468ec-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="468ec-121">RELATED LINKS</span></span>
