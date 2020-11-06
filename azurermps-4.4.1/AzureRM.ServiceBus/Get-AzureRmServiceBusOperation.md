---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusOperation.md
ms.openlocfilehash: fbbac617687712208730393b978a3df5b404aeb5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449509"
---
# <span data-ttu-id="7d257-101">Get-AzureRmServiceBusOperation</span><span class="sxs-lookup"><span data-stu-id="7d257-101">Get-AzureRmServiceBusOperation</span></span>

## <span data-ttu-id="7d257-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7d257-102">SYNOPSIS</span></span>
<span data-ttu-id="7d257-103">清單支援的未列作業</span><span class="sxs-lookup"><span data-stu-id="7d257-103">List supported ServiceBus Operations</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d257-104">句法</span><span class="sxs-lookup"><span data-stu-id="7d257-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusOperation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d257-105">說明</span><span class="sxs-lookup"><span data-stu-id="7d257-105">DESCRIPTION</span></span>
<span data-ttu-id="7d257-106">**AzureRmServiceBusOperation** Cmdlet 會列出未獲支援的作業。</span><span class="sxs-lookup"><span data-stu-id="7d257-106">The **Get-AzureRmServiceBusOperation** cmdlet Lists the ServiceBus supported Operations.</span></span>

## <span data-ttu-id="7d257-107">示例</span><span class="sxs-lookup"><span data-stu-id="7d257-107">EXAMPLES</span></span>

### <span data-ttu-id="7d257-108">範例1</span><span class="sxs-lookup"><span data-stu-id="7d257-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusOperation
```

<span data-ttu-id="7d257-109">列出未受支援的作業</span><span class="sxs-lookup"><span data-stu-id="7d257-109">Lists ServiceBus supported operations</span></span>

## <span data-ttu-id="7d257-110">參數</span><span class="sxs-lookup"><span data-stu-id="7d257-110">PARAMETERS</span></span>

### <span data-ttu-id="7d257-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d257-111">-DefaultProfile</span></span>
<span data-ttu-id="7d257-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7d257-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d257-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d257-113">CommonParameters</span></span>
<span data-ttu-id="7d257-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7d257-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d257-115">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7d257-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d257-116">輸入</span><span class="sxs-lookup"><span data-stu-id="7d257-116">INPUTS</span></span>

### <span data-ttu-id="7d257-117">所有</span><span class="sxs-lookup"><span data-stu-id="7d257-117">None</span></span>

### <span data-ttu-id="7d257-118">[System.object]。清單 ' 1 [0.4.2.0，OperationAttributes，，版本 =，Culture = 中性，PublicKeyToken = null]」））。）</span><span class="sxs-lookup"><span data-stu-id="7d257-118">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.OperationAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.4.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="7d257-119">輸出</span><span class="sxs-lookup"><span data-stu-id="7d257-119">OUTPUTS</span></span>

### <span data-ttu-id="7d257-120">[System.object]。清單 ' 1 [OperationAttributes] 的 [.......]</span><span class="sxs-lookup"><span data-stu-id="7d257-120">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ServiceBus.Models.OperationAttributes]</span></span>

## <span data-ttu-id="7d257-121">筆記</span><span class="sxs-lookup"><span data-stu-id="7d257-121">NOTES</span></span>

## <span data-ttu-id="7d257-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="7d257-122">RELATED LINKS</span></span>

