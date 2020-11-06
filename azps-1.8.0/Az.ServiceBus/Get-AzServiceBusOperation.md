---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusOperation.md
ms.openlocfilehash: ee3ad345bdc5f8eaf18bd9a3d6eeedf5e46de0ab
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620645"
---
# <span data-ttu-id="6db1c-101">Get-AzServiceBusOperation</span><span class="sxs-lookup"><span data-stu-id="6db1c-101">Get-AzServiceBusOperation</span></span>

## <span data-ttu-id="6db1c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6db1c-102">SYNOPSIS</span></span>
<span data-ttu-id="6db1c-103">清單支援的未列作業</span><span class="sxs-lookup"><span data-stu-id="6db1c-103">List supported ServiceBus Operations</span></span>

## <span data-ttu-id="6db1c-104">句法</span><span class="sxs-lookup"><span data-stu-id="6db1c-104">SYNTAX</span></span>

```
Get-AzServiceBusOperation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6db1c-105">說明</span><span class="sxs-lookup"><span data-stu-id="6db1c-105">DESCRIPTION</span></span>
<span data-ttu-id="6db1c-106">**AzServiceBusOperation** Cmdlet 會列出未獲支援的作業。</span><span class="sxs-lookup"><span data-stu-id="6db1c-106">The **Get-AzServiceBusOperation** cmdlet Lists the ServiceBus supported Operations.</span></span>

## <span data-ttu-id="6db1c-107">示例</span><span class="sxs-lookup"><span data-stu-id="6db1c-107">EXAMPLES</span></span>

### <span data-ttu-id="6db1c-108">範例1</span><span class="sxs-lookup"><span data-stu-id="6db1c-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusOperation
```

<span data-ttu-id="6db1c-109">列出未受支援的作業</span><span class="sxs-lookup"><span data-stu-id="6db1c-109">Lists ServiceBus supported operations</span></span>

## <span data-ttu-id="6db1c-110">參數</span><span class="sxs-lookup"><span data-stu-id="6db1c-110">PARAMETERS</span></span>

### <span data-ttu-id="6db1c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6db1c-111">-DefaultProfile</span></span>
<span data-ttu-id="6db1c-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6db1c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6db1c-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6db1c-113">CommonParameters</span></span>
<span data-ttu-id="6db1c-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6db1c-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6db1c-115">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6db1c-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6db1c-116">輸入</span><span class="sxs-lookup"><span data-stu-id="6db1c-116">INPUTS</span></span>

### <span data-ttu-id="6db1c-117">所有</span><span class="sxs-lookup"><span data-stu-id="6db1c-117">None</span></span>

## <span data-ttu-id="6db1c-118">輸出</span><span class="sxs-lookup"><span data-stu-id="6db1c-118">OUTPUTS</span></span>

### <span data-ttu-id="6db1c-119">PSOperationAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6db1c-119">Microsoft.Azure.Commands.ServiceBus.Models.PSOperationAttributes</span></span>

## <span data-ttu-id="6db1c-120">筆記</span><span class="sxs-lookup"><span data-stu-id="6db1c-120">NOTES</span></span>

## <span data-ttu-id="6db1c-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="6db1c-121">RELATED LINKS</span></span>
