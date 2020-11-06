---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusOperation.md
ms.openlocfilehash: e70ff7da7c005f6376d3c4e7a6aae5295e53f693
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451064"
---
# <span data-ttu-id="f2857-101">Get-AzureRmServiceBusOperation</span><span class="sxs-lookup"><span data-stu-id="f2857-101">Get-AzureRmServiceBusOperation</span></span>

## <span data-ttu-id="f2857-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f2857-102">SYNOPSIS</span></span>
<span data-ttu-id="f2857-103">清單支援的未列作業</span><span class="sxs-lookup"><span data-stu-id="f2857-103">List supported ServiceBus Operations</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2857-104">句法</span><span class="sxs-lookup"><span data-stu-id="f2857-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusOperation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2857-105">說明</span><span class="sxs-lookup"><span data-stu-id="f2857-105">DESCRIPTION</span></span>
<span data-ttu-id="f2857-106">**AzureRmServiceBusOperation** Cmdlet 會列出未獲支援的作業。</span><span class="sxs-lookup"><span data-stu-id="f2857-106">The **Get-AzureRmServiceBusOperation** cmdlet Lists the ServiceBus supported Operations.</span></span>

## <span data-ttu-id="f2857-107">示例</span><span class="sxs-lookup"><span data-stu-id="f2857-107">EXAMPLES</span></span>

### <span data-ttu-id="f2857-108">範例1</span><span class="sxs-lookup"><span data-stu-id="f2857-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusOperation
```

<span data-ttu-id="f2857-109">列出未受支援的作業</span><span class="sxs-lookup"><span data-stu-id="f2857-109">Lists ServiceBus supported operations</span></span>

## <span data-ttu-id="f2857-110">參數</span><span class="sxs-lookup"><span data-stu-id="f2857-110">PARAMETERS</span></span>

### <span data-ttu-id="f2857-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2857-111">-DefaultProfile</span></span>
<span data-ttu-id="f2857-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f2857-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2857-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2857-113">CommonParameters</span></span>
<span data-ttu-id="f2857-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f2857-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2857-115">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f2857-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2857-116">輸入</span><span class="sxs-lookup"><span data-stu-id="f2857-116">INPUTS</span></span>

### <span data-ttu-id="f2857-117">所有</span><span class="sxs-lookup"><span data-stu-id="f2857-117">None</span></span>

## <span data-ttu-id="f2857-118">輸出</span><span class="sxs-lookup"><span data-stu-id="f2857-118">OUTPUTS</span></span>

### <span data-ttu-id="f2857-119">PSOperationAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f2857-119">Microsoft.Azure.Commands.ServiceBus.Models.PSOperationAttributes</span></span>

## <span data-ttu-id="f2857-120">筆記</span><span class="sxs-lookup"><span data-stu-id="f2857-120">NOTES</span></span>

## <span data-ttu-id="f2857-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="f2857-121">RELATED LINKS</span></span>
