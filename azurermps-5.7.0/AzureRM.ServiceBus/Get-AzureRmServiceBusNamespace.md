---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 2584630c8c1d0981f354ffc920af4f8ed9ff979f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447644"
---
# <span data-ttu-id="fe645-101">Get-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="fe645-101">Get-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="fe645-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fe645-102">SYNOPSIS</span></span>
<span data-ttu-id="fe645-103">取得資源群組中指定服務匯流排命名空間的描述。</span><span class="sxs-lookup"><span data-stu-id="fe645-103">Gets a description for the specified Service Bus namespace within the resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe645-104">句法</span><span class="sxs-lookup"><span data-stu-id="fe645-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe645-105">說明</span><span class="sxs-lookup"><span data-stu-id="fe645-105">DESCRIPTION</span></span>
<span data-ttu-id="fe645-106">**AzureRmServiceBusNamespace** Cmdlet 會取得資源群組中指定服務匯流排命名空間的描述。</span><span class="sxs-lookup"><span data-stu-id="fe645-106">The **Get-AzureRmServiceBusNamespace** cmdlet gets a description for the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="fe645-107">示例</span><span class="sxs-lookup"><span data-stu-id="fe645-107">EXAMPLES</span></span>

### <span data-ttu-id="fe645-108">範例1</span><span class="sxs-lookup"><span data-stu-id="fe645-108">Example 1</span></span>

```
PS C:\> Get-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1

Name               : SB-Example1
Id                 : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
Location           : West US
Sku                : Name : Standard , Capacity : 1 , Tier : Standard
ProvisioningState  : Succeeded
CreatedAt          : 1/20/2017 1:40:01 AM
UpdatedAt          : 1/20/2017 1:40:24 AM
ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/

```

## <span data-ttu-id="fe645-109">參數</span><span class="sxs-lookup"><span data-stu-id="fe645-109">PARAMETERS</span></span>

### <span data-ttu-id="fe645-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe645-110">-DefaultProfile</span></span>
<span data-ttu-id="fe645-111">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fe645-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe645-112">-名稱</span><span class="sxs-lookup"><span data-stu-id="fe645-112">-Name</span></span>
<span data-ttu-id="fe645-113">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="fe645-113">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe645-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe645-114">-ResourceGroupName</span></span>
<span data-ttu-id="fe645-115">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="fe645-115">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe645-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe645-116">CommonParameters</span></span>
<span data-ttu-id="fe645-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fe645-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe645-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fe645-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe645-119">輸入</span><span class="sxs-lookup"><span data-stu-id="fe645-119">INPUTS</span></span>

### <span data-ttu-id="fe645-120">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="fe645-120">-ResourceGroup</span></span>
<span data-ttu-id="fe645-121">System.object</span><span class="sxs-lookup"><span data-stu-id="fe645-121">System.String</span></span>

### <span data-ttu-id="fe645-122">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="fe645-122">-NamespaceName</span></span>
 <span data-ttu-id="fe645-123">System.object</span><span class="sxs-lookup"><span data-stu-id="fe645-123">System.String</span></span>

## <span data-ttu-id="fe645-124">輸出</span><span class="sxs-lookup"><span data-stu-id="fe645-124">OUTPUTS</span></span>

### <span data-ttu-id="fe645-125">[System.object]。清單 ' 1 [0.0.1.0，PSNamespaceAttributes，，版本 =，Culture = 中性，PublicKeyToken = null]」））。）</span><span class="sxs-lookup"><span data-stu-id="fe645-125">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="fe645-126">筆記</span><span class="sxs-lookup"><span data-stu-id="fe645-126">NOTES</span></span>

## <span data-ttu-id="fe645-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="fe645-127">RELATED LINKS</span></span>

