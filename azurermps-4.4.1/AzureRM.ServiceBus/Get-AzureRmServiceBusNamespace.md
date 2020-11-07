---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 2e6e044d888386b56d04ad48b7fbdaedadbd7497
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623640"
---
# <span data-ttu-id="03f10-101">Get-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="03f10-101">Get-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="03f10-102">摘要</span><span class="sxs-lookup"><span data-stu-id="03f10-102">SYNOPSIS</span></span>
<span data-ttu-id="03f10-103">取得資源群組中指定服務匯流排命名空間的描述。</span><span class="sxs-lookup"><span data-stu-id="03f10-103">Gets a description for the specified Service Bus namespace within the resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03f10-104">句法</span><span class="sxs-lookup"><span data-stu-id="03f10-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusNamespace [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03f10-105">說明</span><span class="sxs-lookup"><span data-stu-id="03f10-105">DESCRIPTION</span></span>
<span data-ttu-id="03f10-106">**AzureRmServiceBusNamespace** Cmdlet 會取得資源群組中指定服務匯流排命名空間的描述。</span><span class="sxs-lookup"><span data-stu-id="03f10-106">The **Get-AzureRmServiceBusNamespace** cmdlet gets a description for the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="03f10-107">示例</span><span class="sxs-lookup"><span data-stu-id="03f10-107">EXAMPLES</span></span>

### <span data-ttu-id="03f10-108">範例1</span><span class="sxs-lookup"><span data-stu-id="03f10-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="03f10-109">傳回指定服務匯流排命名空間的描述。</span><span class="sxs-lookup"><span data-stu-id="03f10-109">Returns a description of the specified Service Bus namespace.</span></span>

## <span data-ttu-id="03f10-110">參數</span><span class="sxs-lookup"><span data-stu-id="03f10-110">PARAMETERS</span></span>

### <span data-ttu-id="03f10-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03f10-111">-DefaultProfile</span></span>
<span data-ttu-id="03f10-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="03f10-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03f10-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="03f10-113">-Name</span></span>
<span data-ttu-id="03f10-114">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="03f10-114">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03f10-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03f10-115">-ResourceGroupName</span></span>
<span data-ttu-id="03f10-116">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="03f10-116">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03f10-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03f10-117">CommonParameters</span></span>
<span data-ttu-id="03f10-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="03f10-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03f10-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="03f10-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03f10-120">輸入</span><span class="sxs-lookup"><span data-stu-id="03f10-120">INPUTS</span></span>

### <span data-ttu-id="03f10-121">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="03f10-121">-ResourceGroup</span></span>
<span data-ttu-id="03f10-122">System.object</span><span class="sxs-lookup"><span data-stu-id="03f10-122">System.String</span></span>

### <span data-ttu-id="03f10-123">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="03f10-123">-NamespaceName</span></span>
 <span data-ttu-id="03f10-124">System.object</span><span class="sxs-lookup"><span data-stu-id="03f10-124">System.String</span></span>

## <span data-ttu-id="03f10-125">輸出</span><span class="sxs-lookup"><span data-stu-id="03f10-125">OUTPUTS</span></span>

### <span data-ttu-id="03f10-126">[System.object]。清單 ' 1 [0.0.1.0，NamespaceAttributes，，版本 =，Culture = 中性，PublicKeyToken = null]」））。）</span><span class="sxs-lookup"><span data-stu-id="03f10-126">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.NamespaceAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="03f10-127">名稱： SB-Example1 識別碼：/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1 位置：美國西部 Sku： Name： Standard，容量：1，層：標準 ProvisioningState：成功狀態：使用中 CreatedAt： 1/20/2017 1:40:01 AM UpdatedAt： 1/20/2017 1:40:24 AM ServiceBusEndpoint： https://SB-Example1.servicebus.windows.net:443/ Enabled： True</span><span class="sxs-lookup"><span data-stu-id="03f10-127">Name               : SB-Example1 Id                 : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1 Location           : West US Sku                : Name : Standard , Capacity : 1 , Tier : Standard ProvisioningState  : Succeeded Status             : Active CreatedAt          : 1/20/2017 1:40:01 AM UpdatedAt          : 1/20/2017 1:40:24 AM ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/ Enabled            : True</span></span>

## <span data-ttu-id="03f10-128">筆記</span><span class="sxs-lookup"><span data-stu-id="03f10-128">NOTES</span></span>
## <span data-ttu-id="03f10-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="03f10-129">RELATED LINKS</span></span>

## <span data-ttu-id="03f10-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="03f10-130">RELATED LINKS</span></span>

