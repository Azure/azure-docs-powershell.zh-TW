---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNamespace.md
ms.openlocfilehash: 1e4e1d50df44715fe433a5106619264063b2f22e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620647"
---
# <span data-ttu-id="06c4d-101">Get-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="06c4d-101">Get-AzServiceBusNamespace</span></span>

## <span data-ttu-id="06c4d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="06c4d-102">SYNOPSIS</span></span>
<span data-ttu-id="06c4d-103">取得資源群組中指定服務匯流排命名空間的描述。</span><span class="sxs-lookup"><span data-stu-id="06c4d-103">Gets a description for the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="06c4d-104">句法</span><span class="sxs-lookup"><span data-stu-id="06c4d-104">SYNTAX</span></span>

```
Get-AzServiceBusNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06c4d-105">說明</span><span class="sxs-lookup"><span data-stu-id="06c4d-105">DESCRIPTION</span></span>
<span data-ttu-id="06c4d-106">**AzServiceBusNamespace** Cmdlet 會取得資源群組中指定服務匯流排命名空間的描述。</span><span class="sxs-lookup"><span data-stu-id="06c4d-106">The **Get-AzServiceBusNamespace** cmdlet gets a description for the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="06c4d-107">示例</span><span class="sxs-lookup"><span data-stu-id="06c4d-107">EXAMPLES</span></span>

### <span data-ttu-id="06c4d-108">範例1</span><span class="sxs-lookup"><span data-stu-id="06c4d-108">Example 1</span></span>

```
PS C:\> Get-AzServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1

Name               : SB-Example1
Id                 : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
ResourceGroup      : Default-ServiceBus-WestUS
Location           : West US
Tags               : {TesttingTags, TestingTagValue, TestTag, TestTagValue}
Sku                : Name : Premium , Tier : Premium
ProvisioningState  : Succeeded
CreatedAt          : 1/20/2017 1:40:01 AM
UpdatedAt          : 1/20/2017 1:40:24 AM
ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/
```

## <span data-ttu-id="06c4d-109">參數</span><span class="sxs-lookup"><span data-stu-id="06c4d-109">PARAMETERS</span></span>

### <span data-ttu-id="06c4d-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06c4d-110">-DefaultProfile</span></span>
<span data-ttu-id="06c4d-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="06c4d-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06c4d-112">-名稱</span><span class="sxs-lookup"><span data-stu-id="06c4d-112">-Name</span></span>
<span data-ttu-id="06c4d-113">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="06c4d-113">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06c4d-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06c4d-114">-ResourceGroupName</span></span>
<span data-ttu-id="06c4d-115">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="06c4d-115">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06c4d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06c4d-116">CommonParameters</span></span>
<span data-ttu-id="06c4d-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="06c4d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06c4d-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="06c4d-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06c4d-119">輸入</span><span class="sxs-lookup"><span data-stu-id="06c4d-119">INPUTS</span></span>

### <span data-ttu-id="06c4d-120">System.object</span><span class="sxs-lookup"><span data-stu-id="06c4d-120">System.String</span></span>

## <span data-ttu-id="06c4d-121">輸出</span><span class="sxs-lookup"><span data-stu-id="06c4d-121">OUTPUTS</span></span>

### <span data-ttu-id="06c4d-122">PSNamespaceAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="06c4d-122">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="06c4d-123">筆記</span><span class="sxs-lookup"><span data-stu-id="06c4d-123">NOTES</span></span>

## <span data-ttu-id="06c4d-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="06c4d-124">RELATED LINKS</span></span>
