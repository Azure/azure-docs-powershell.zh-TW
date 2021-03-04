---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/get-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNamespace.md
ms.openlocfilehash: ef4d7ccf2f56d8a6d2a70fa4efb9468365cfcd32
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912601"
---
# <span data-ttu-id="5d81a-101">Get-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="5d81a-101">Get-AzServiceBusNamespace</span></span>

## <span data-ttu-id="5d81a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5d81a-102">SYNOPSIS</span></span>
<span data-ttu-id="5d81a-103">在資源群組中，為指定的 Service Bus 命名空間獲得描述。</span><span class="sxs-lookup"><span data-stu-id="5d81a-103">Gets a description for the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="5d81a-104">語法</span><span class="sxs-lookup"><span data-stu-id="5d81a-104">SYNTAX</span></span>

```
Get-AzServiceBusNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d81a-105">描述</span><span class="sxs-lookup"><span data-stu-id="5d81a-105">DESCRIPTION</span></span>
<span data-ttu-id="5d81a-106">**Get-AzServiceBusNamespace** Cmdlet 會取得資源群組中指定 Service Bus 命名空間的描述。</span><span class="sxs-lookup"><span data-stu-id="5d81a-106">The **Get-AzServiceBusNamespace** cmdlet gets a description for the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="5d81a-107">例子</span><span class="sxs-lookup"><span data-stu-id="5d81a-107">EXAMPLES</span></span>

### <span data-ttu-id="5d81a-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="5d81a-108">Example 1</span></span>

```
PS C:\> Get-AzServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1

Name               : SB-Example1
Id                 : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
ResourceGroupName  : Default-ServiceBus-WestUS
Location           : West US
Tags               : {TesttingTags, TestingTagValue, TestTag, TestTagValue}
Sku                : Name : Premium , Tier : Premium
ProvisioningState  : Succeeded
CreatedAt          : 1/20/2017 1:40:01 AM
UpdatedAt          : 1/20/2017 1:40:24 AM
ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/
```

## <span data-ttu-id="5d81a-109">參數</span><span class="sxs-lookup"><span data-stu-id="5d81a-109">PARAMETERS</span></span>

### <span data-ttu-id="5d81a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d81a-110">-DefaultProfile</span></span>
<span data-ttu-id="5d81a-111">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5d81a-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d81a-112">-名稱</span><span class="sxs-lookup"><span data-stu-id="5d81a-112">-Name</span></span>
<span data-ttu-id="5d81a-113">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="5d81a-113">Namespace Name.</span></span>

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

### <span data-ttu-id="5d81a-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d81a-114">-ResourceGroupName</span></span>
<span data-ttu-id="5d81a-115">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="5d81a-115">The name of the resource group</span></span>

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

### <span data-ttu-id="5d81a-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d81a-116">CommonParameters</span></span>
<span data-ttu-id="5d81a-117">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5d81a-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d81a-118">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="5d81a-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d81a-119">輸入</span><span class="sxs-lookup"><span data-stu-id="5d81a-119">INPUTS</span></span>

### <span data-ttu-id="5d81a-120">System.String</span><span class="sxs-lookup"><span data-stu-id="5d81a-120">System.String</span></span>

## <span data-ttu-id="5d81a-121">輸出</span><span class="sxs-lookup"><span data-stu-id="5d81a-121">OUTPUTS</span></span>

### <span data-ttu-id="5d81a-122">Microsoft.Azure.Commands.ServiceBus.models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="5d81a-122">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="5d81a-123">筆記</span><span class="sxs-lookup"><span data-stu-id="5d81a-123">NOTES</span></span>

## <span data-ttu-id="5d81a-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="5d81a-124">RELATED LINKS</span></span>
