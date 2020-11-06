---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespaceKey.md
ms.openlocfilehash: 87dc2d1e372bdab6415a78e8c79ed0c3bd5491ed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449508"
---
# <span data-ttu-id="f533f-101">Get-AzureRmServiceBusNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="f533f-101">Get-AzureRmServiceBusNamespaceKey</span></span>

## <span data-ttu-id="f533f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f533f-102">SYNOPSIS</span></span>
<span data-ttu-id="f533f-103">取得命名空間的主要和次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="f533f-103">Gets the primary and secondary connection strings for the namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f533f-104">句法</span><span class="sxs-lookup"><span data-stu-id="f533f-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusNamespaceKey [-ResourceGroup] <String> -Namespace <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f533f-105">說明</span><span class="sxs-lookup"><span data-stu-id="f533f-105">DESCRIPTION</span></span>
<span data-ttu-id="f533f-106">**AzureRmServiceBusNamespaceKey** Cmdlet 會傳回指定命名空間的主要和次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="f533f-106">The **Get-AzureRmServiceBusNamespaceKey** cmdlet returns the primary and secondary connection strings for the given namespace.</span></span> 

## <span data-ttu-id="f533f-107">示例</span><span class="sxs-lookup"><span data-stu-id="f533f-107">EXAMPLES</span></span>

### <span data-ttu-id="f533f-108">範例1</span><span class="sxs-lookup"><span data-stu-id="f533f-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusNamespaceKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthorizationRuleName AuthoRule1
```

<span data-ttu-id="f533f-109">在指定命名空間中的主要和次要連線字串。</span><span class="sxs-lookup"><span data-stu-id="f533f-109">Primary and secondary connection string to the specified namespace.</span></span>

## <span data-ttu-id="f533f-110">參數</span><span class="sxs-lookup"><span data-stu-id="f533f-110">PARAMETERS</span></span>

### <span data-ttu-id="f533f-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f533f-111">-ResourceGroup</span></span>
<span data-ttu-id="f533f-112">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f533f-112">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f533f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f533f-113">-DefaultProfile</span></span>
<span data-ttu-id="f533f-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f533f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f533f-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="f533f-115">-Name</span></span>
<span data-ttu-id="f533f-116">[AuthorizationRule] 命名空間的名稱。</span><span class="sxs-lookup"><span data-stu-id="f533f-116">ServiceBus Namespace AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f533f-117">-命名空間</span><span class="sxs-lookup"><span data-stu-id="f533f-117">-Namespace</span></span>
<span data-ttu-id="f533f-118">已將命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="f533f-118">ServiceBus Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f533f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f533f-119">CommonParameters</span></span>
<span data-ttu-id="f533f-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f533f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f533f-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f533f-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f533f-122">輸入</span><span class="sxs-lookup"><span data-stu-id="f533f-122">INPUTS</span></span>

### <span data-ttu-id="f533f-123">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f533f-123">-ResourceGroup</span></span>
 <span data-ttu-id="f533f-124">System.object</span><span class="sxs-lookup"><span data-stu-id="f533f-124">System.String</span></span>
 

### <span data-ttu-id="f533f-125">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="f533f-125">-NamespaceName</span></span>
 <span data-ttu-id="f533f-126">System.object</span><span class="sxs-lookup"><span data-stu-id="f533f-126">System.String</span></span>
 

### <span data-ttu-id="f533f-127">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="f533f-127">-AuthorizationRuleName</span></span>
 <span data-ttu-id="f533f-128">System.object</span><span class="sxs-lookup"><span data-stu-id="f533f-128">System.String</span></span>

## <span data-ttu-id="f533f-129">輸出</span><span class="sxs-lookup"><span data-stu-id="f533f-129">OUTPUTS</span></span>

### <span data-ttu-id="f533f-130">ResourceListKeys （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="f533f-130">Microsoft.Azure.Management.ServiceBus.Models.ResourceListKeys</span></span>
<span data-ttu-id="f533f-131">PrimaryConnectionString： Endpoint = sb：//sb-example1.servicebus.windows.net/;SharedAccessKeyName = AuthoRule1;SharedAccessKey = {SharedAccessKey 值} SecondaryConnectionString： Endpoint = sb：//sb-example1.servicebus.windows.net/;SharedAccessKeyName = AuthoRule1;SharedAccessKey = {SharedAccessKey value} PrimaryKey： {PrimaryKey 值} SecondaryKey： {SecondaryKey 值} KeyName： AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="f533f-131">PrimaryConnectionString   : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey={SharedAccessKey value} SecondaryConnectionString : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=AuthoRule1;SharedAccessKey={SharedAccessKey value} PrimaryKey                : {PrimaryKey value} SecondaryKey              : {SecondaryKey value} KeyName                   : AuthoRule1</span></span>

## <span data-ttu-id="f533f-132">筆記</span><span class="sxs-lookup"><span data-stu-id="f533f-132">NOTES</span></span>

## <span data-ttu-id="f533f-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="f533f-133">RELATED LINKS</span></span>

