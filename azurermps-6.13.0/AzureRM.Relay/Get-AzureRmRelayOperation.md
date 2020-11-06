---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/get-azurermrelayoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayOperation.md
ms.openlocfilehash: e7f45be6a39cdd2b7f2d11736d2a5f62831244c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448268"
---
# <span data-ttu-id="14329-101">Get-AzureRmRelayOperation</span><span class="sxs-lookup"><span data-stu-id="14329-101">Get-AzureRmRelayOperation</span></span>

## <span data-ttu-id="14329-102">摘要</span><span class="sxs-lookup"><span data-stu-id="14329-102">SYNOPSIS</span></span>
<span data-ttu-id="14329-103">清單支援的中繼作業</span><span class="sxs-lookup"><span data-stu-id="14329-103">List supported Relay Operations</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14329-104">句法</span><span class="sxs-lookup"><span data-stu-id="14329-104">SYNTAX</span></span>

```
Get-AzureRmRelayOperation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14329-105">說明</span><span class="sxs-lookup"><span data-stu-id="14329-105">DESCRIPTION</span></span>
<span data-ttu-id="14329-106">**AzureRmRelayOperation** Cmdlet 會列出中繼支援的作業。</span><span class="sxs-lookup"><span data-stu-id="14329-106">The **Get-AzureRmRelayOperation** cmdlet Lists the Relay supported Operations.</span></span>

## <span data-ttu-id="14329-107">示例</span><span class="sxs-lookup"><span data-stu-id="14329-107">EXAMPLES</span></span>

### <span data-ttu-id="14329-108">範例1</span><span class="sxs-lookup"><span data-stu-id="14329-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRelayOperation

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

<span data-ttu-id="14329-109">列出中繼支援的作業</span><span class="sxs-lookup"><span data-stu-id="14329-109">Lists Relay supported operations</span></span>

## <span data-ttu-id="14329-110">參數</span><span class="sxs-lookup"><span data-stu-id="14329-110">PARAMETERS</span></span>

### <span data-ttu-id="14329-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14329-111">-DefaultProfile</span></span>
<span data-ttu-id="14329-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="14329-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14329-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14329-113">CommonParameters</span></span>
<span data-ttu-id="14329-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="14329-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="14329-115">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="14329-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14329-116">輸入</span><span class="sxs-lookup"><span data-stu-id="14329-116">INPUTS</span></span>

### <span data-ttu-id="14329-117">所有</span><span class="sxs-lookup"><span data-stu-id="14329-117">None</span></span>


## <span data-ttu-id="14329-118">輸出</span><span class="sxs-lookup"><span data-stu-id="14329-118">OUTPUTS</span></span>

### <span data-ttu-id="14329-119">PSOperationAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="14329-119">Microsoft.Azure.Commands.Relay.Models.PSOperationAttributes</span></span>


## <span data-ttu-id="14329-120">筆記</span><span class="sxs-lookup"><span data-stu-id="14329-120">NOTES</span></span>

## <span data-ttu-id="14329-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="14329-121">RELATED LINKS</span></span>
