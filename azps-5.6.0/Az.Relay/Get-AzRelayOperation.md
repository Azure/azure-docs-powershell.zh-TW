---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/get-azrelayoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayOperation.md
ms.openlocfilehash: 72f9e3290af5aad665213c1ffdebf5f3b2edcf92
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914605"
---
# <span data-ttu-id="45140-101">Get-AzRelayOperation</span><span class="sxs-lookup"><span data-stu-id="45140-101">Get-AzRelayOperation</span></span>

## <span data-ttu-id="45140-102">簡介</span><span class="sxs-lookup"><span data-stu-id="45140-102">SYNOPSIS</span></span>
<span data-ttu-id="45140-103">清單支援的轉場作業</span><span class="sxs-lookup"><span data-stu-id="45140-103">List supported Relay Operations</span></span>

## <span data-ttu-id="45140-104">語法</span><span class="sxs-lookup"><span data-stu-id="45140-104">SYNTAX</span></span>

```
Get-AzRelayOperation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45140-105">描述</span><span class="sxs-lookup"><span data-stu-id="45140-105">DESCRIPTION</span></span>
<span data-ttu-id="45140-106">**Get-AzRelayOperation Cmdlet** 會列出轉場支援的作業。</span><span class="sxs-lookup"><span data-stu-id="45140-106">The **Get-AzRelayOperation** cmdlet Lists the Relay supported Operations.</span></span>

## <span data-ttu-id="45140-107">例子</span><span class="sxs-lookup"><span data-stu-id="45140-107">EXAMPLES</span></span>

### <span data-ttu-id="45140-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="45140-108">Example 1</span></span>
```
PS C:\> Get-AzRelayOperation

Name                                                                            Display
----                                                                            -------
Microsoft.Relay/checkNamespaceAvailability/action                               Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/register/action                                                 Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/write                                                Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/read                                                 Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/Delete                                               Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/authorizationRules/write                             Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/authorizationRules/delete                            Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/authorizationRules/listkeys/action                   Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/write                              Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/read                               Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/Delete                             Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/authorizationRules/write           Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/authorizationRules/delete          Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/authorizationRules/listkeys/action Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/write                                      Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/read                                       Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/Delete                                     Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/authorizationRules/write                   Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/authorizationRules/delete                  Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/authorizationRules/listkeys/action         Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
```

<span data-ttu-id="45140-109">清單轉場支援的作業</span><span class="sxs-lookup"><span data-stu-id="45140-109">Lists Relay supported operations</span></span>

## <span data-ttu-id="45140-110">參數</span><span class="sxs-lookup"><span data-stu-id="45140-110">PARAMETERS</span></span>

### <span data-ttu-id="45140-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45140-111">-DefaultProfile</span></span>
<span data-ttu-id="45140-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="45140-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45140-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45140-113">CommonParameters</span></span>
<span data-ttu-id="45140-114">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="45140-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45140-115">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="45140-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45140-116">輸入</span><span class="sxs-lookup"><span data-stu-id="45140-116">INPUTS</span></span>

### <span data-ttu-id="45140-117">沒有</span><span class="sxs-lookup"><span data-stu-id="45140-117">None</span></span>

## <span data-ttu-id="45140-118">輸出</span><span class="sxs-lookup"><span data-stu-id="45140-118">OUTPUTS</span></span>

### <span data-ttu-id="45140-119">Microsoft.Azure.Commands.Relay.models.PSOperationAttributes</span><span class="sxs-lookup"><span data-stu-id="45140-119">Microsoft.Azure.Commands.Relay.Models.PSOperationAttributes</span></span>

## <span data-ttu-id="45140-120">筆記</span><span class="sxs-lookup"><span data-stu-id="45140-120">NOTES</span></span>

## <span data-ttu-id="45140-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="45140-121">RELATED LINKS</span></span>
