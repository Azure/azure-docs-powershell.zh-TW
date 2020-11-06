---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopicKey.md
ms.openlocfilehash: 24041c299f2f242126f265ad232db3e0c5d526b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454855"
---
# <span data-ttu-id="875b1-101">Get-AzureRmServiceBusTopicKey</span><span class="sxs-lookup"><span data-stu-id="875b1-101">Get-AzureRmServiceBusTopicKey</span></span>

## <span data-ttu-id="875b1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="875b1-102">SYNOPSIS</span></span>
<span data-ttu-id="875b1-103">取得服務匯流排主題的主要和次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="875b1-103">Gets the primary and secondary connection strings for the Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="875b1-104">句法</span><span class="sxs-lookup"><span data-stu-id="875b1-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusTopicKey [-ResourceGroup] <String> -Namespace <String> -Topic <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="875b1-105">說明</span><span class="sxs-lookup"><span data-stu-id="875b1-105">DESCRIPTION</span></span>
<span data-ttu-id="875b1-106">**AzureRmServiceBusTopicKey** Cmdlet 會傳回指定服務匯流排主題的主要和次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="875b1-106">The **Get-AzureRmServiceBusTopicKey** cmdlet returns the primary and secondary connection strings for the given Service Bus topic.</span></span>

## <span data-ttu-id="875b1-107">示例</span><span class="sxs-lookup"><span data-stu-id="875b1-107">EXAMPLES</span></span>

### <span data-ttu-id="875b1-108">範例1</span><span class="sxs-lookup"><span data-stu-id="875b1-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusTopicKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1
```

<span data-ttu-id="875b1-109">傳回指定服務匯流排主題的主要和次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="875b1-109">Returns the primary and secondary connection strings for the specified Service Bus topic.</span></span>

## <span data-ttu-id="875b1-110">參數</span><span class="sxs-lookup"><span data-stu-id="875b1-110">PARAMETERS</span></span>

### <span data-ttu-id="875b1-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="875b1-111">-ResourceGroup</span></span>
<span data-ttu-id="875b1-112">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="875b1-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="875b1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="875b1-113">-DefaultProfile</span></span>
<span data-ttu-id="875b1-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="875b1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="875b1-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="875b1-115">-Name</span></span>
<span data-ttu-id="875b1-116">主題 AuthorizationRule 名稱。</span><span class="sxs-lookup"><span data-stu-id="875b1-116">Topic AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="875b1-117">-命名空間</span><span class="sxs-lookup"><span data-stu-id="875b1-117">-Namespace</span></span>
<span data-ttu-id="875b1-118">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="875b1-118">Namespace Name.</span></span>

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

### <span data-ttu-id="875b1-119">-主題</span><span class="sxs-lookup"><span data-stu-id="875b1-119">-Topic</span></span>
<span data-ttu-id="875b1-120">主題名稱。</span><span class="sxs-lookup"><span data-stu-id="875b1-120">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="875b1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="875b1-121">CommonParameters</span></span>
<span data-ttu-id="875b1-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="875b1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="875b1-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="875b1-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="875b1-124">輸入</span><span class="sxs-lookup"><span data-stu-id="875b1-124">INPUTS</span></span>

### <span data-ttu-id="875b1-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="875b1-125">-ResourceGroup</span></span>
 <span data-ttu-id="875b1-126">System.object</span><span class="sxs-lookup"><span data-stu-id="875b1-126">System.String</span></span>
 

### <span data-ttu-id="875b1-127">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="875b1-127">-NamespaceName</span></span>
 <span data-ttu-id="875b1-128">System.object</span><span class="sxs-lookup"><span data-stu-id="875b1-128">System.String</span></span>
 

### <span data-ttu-id="875b1-129">-TopicName</span><span class="sxs-lookup"><span data-stu-id="875b1-129">-TopicName</span></span>
 <span data-ttu-id="875b1-130">System.object</span><span class="sxs-lookup"><span data-stu-id="875b1-130">System.String</span></span>
 

### <span data-ttu-id="875b1-131">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="875b1-131">-AuthorizationRuleName</span></span>
 <span data-ttu-id="875b1-132">System.object</span><span class="sxs-lookup"><span data-stu-id="875b1-132">System.String</span></span>

## <span data-ttu-id="875b1-133">輸出</span><span class="sxs-lookup"><span data-stu-id="875b1-133">OUTPUTS</span></span>

### <span data-ttu-id="875b1-134">ListKeysAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="875b1-134">Microsoft.Azure.Commands.ServiceBus.Models.ListKeysAttributes</span></span>
<span data-ttu-id="875b1-135">PrimaryConnectionString： Endpoint = sb：//sb-example1.servicebus.windows.net/;SharedAccessKeyName = SBTopicAuthoRule1;SharedAccessKey = {SharedAccessKey 值};EntityPath = SB-To pic_exampl1 SecondaryConnectionString： Endpoint = sb：//sb-example1.servicebus.windows.net/;SharedAccessKeyName = SBTopicAuthoRule1;SharedAccessKey = {SharedAccessKey 值};EntityPath = SB-To pic_exampl1 PrimaryKey： {PrimaryKey 值} SecondaryKey： {SecondaryKey 值} KeyName： SBTopicAuthoRule1</span><span class="sxs-lookup"><span data-stu-id="875b1-135">PrimaryConnectionString   : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBTopicAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-To pic_exampl1 SecondaryConnectionString : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBTopicAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-To pic_exampl1 PrimaryKey                : {PrimaryKey value} SecondaryKey              : {SecondaryKey value} KeyName                   : SBTopicAuthoRule1</span></span>

## <span data-ttu-id="875b1-136">筆記</span><span class="sxs-lookup"><span data-stu-id="875b1-136">NOTES</span></span>

## <span data-ttu-id="875b1-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="875b1-137">RELATED LINKS</span></span>

