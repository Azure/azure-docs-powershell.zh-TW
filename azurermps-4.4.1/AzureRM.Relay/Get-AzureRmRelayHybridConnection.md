---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 2fccb11ba45fa1d532c35140db588294895c0802
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448021"
---
# <span data-ttu-id="0124b-101">Get-AzureRmRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="0124b-101">Get-AzureRmRelayHybridConnection</span></span>

## <span data-ttu-id="0124b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0124b-102">SYNOPSIS</span></span>
<span data-ttu-id="0124b-103">取得中繼命名空間中指定 HybridConnection 的描述。</span><span class="sxs-lookup"><span data-stu-id="0124b-103">Gets a description for the specified HybridConnection within the Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0124b-104">句法</span><span class="sxs-lookup"><span data-stu-id="0124b-104">SYNTAX</span></span>

```
Get-AzureRmRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0124b-105">說明</span><span class="sxs-lookup"><span data-stu-id="0124b-105">DESCRIPTION</span></span>
<span data-ttu-id="0124b-106">**AzureRmRelayHybridConnection** Cmdlet 會取得中繼命名空間中指定 HybridConnection 的描述。</span><span class="sxs-lookup"><span data-stu-id="0124b-106">The **Get-AzureRmRelayHybridConnection** cmdlet gets a description for the specified HybridConnection within the Relay namespace.</span></span>

## <span data-ttu-id="0124b-107">示例</span><span class="sxs-lookup"><span data-stu-id="0124b-107">EXAMPLES</span></span>

### <span data-ttu-id="0124b-108">範例1</span><span class="sxs-lookup"><span data-stu-id="0124b-108">Example 1</span></span>
```
PS C:\>Get-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
```

<span data-ttu-id="0124b-109">傳回 HybridConnection 的描述。</span><span class="sxs-lookup"><span data-stu-id="0124b-109">Returns the description of the HybridConnection.</span></span> 

## <span data-ttu-id="0124b-110">參數</span><span class="sxs-lookup"><span data-stu-id="0124b-110">PARAMETERS</span></span>

### <span data-ttu-id="0124b-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="0124b-111">-Name</span></span>
<span data-ttu-id="0124b-112">HybridConnections [名稱]。</span><span class="sxs-lookup"><span data-stu-id="0124b-112">HybridConnections Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0124b-113">-命名空間</span><span class="sxs-lookup"><span data-stu-id="0124b-113">-Namespace</span></span>
<span data-ttu-id="0124b-114">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="0124b-114">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0124b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0124b-115">-ResourceGroupName</span></span>
<span data-ttu-id="0124b-116">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="0124b-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="0124b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0124b-117">-DefaultProfile</span></span>
<span data-ttu-id="0124b-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0124b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0124b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0124b-119">CommonParameters</span></span>
<span data-ttu-id="0124b-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0124b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0124b-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0124b-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0124b-122">輸入</span><span class="sxs-lookup"><span data-stu-id="0124b-122">INPUTS</span></span>

### <span data-ttu-id="0124b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0124b-123">-ResourceGroupName</span></span>
    System.String

### <span data-ttu-id="0124b-124">-命名空間</span><span class="sxs-lookup"><span data-stu-id="0124b-124">-Namespace</span></span>
    System.String

### <span data-ttu-id="0124b-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="0124b-125">-Name</span></span>
    System.String

## <span data-ttu-id="0124b-126">輸出</span><span class="sxs-lookup"><span data-stu-id="0124b-126">OUTPUTS</span></span>

### <span data-ttu-id="0124b-127">[System.object]. 清單 ' 1 [HybridConnectionAttibutes，0.1.0.0，#.. 繼電器，版本 =，Culture = 中性，PublicKeyToken = null]]。</span><span class="sxs-lookup"><span data-stu-id="0124b-127">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="0124b-128">CreatedAt： 4/12/2017 3:17:02 上午 UpdatedAt： 4/12/2017 3:17:02 AM ListenerCount： 0 RequiresClientAuthorization： True UserMetadata： User 中繼資料識別碼：/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/H ybridConnections/TestHybridConnection Name： TestHybridConnection 類型： Microsoft. 中繼/HybridConnections</span><span class="sxs-lookup"><span data-stu-id="0124b-128">CreatedAt                   : 4/12/2017 3:17:02 AM UpdatedAt                   : 4/12/2017 3:17:02 AM ListenerCount               : 0 RequiresClientAuthorization : True UserMetadata                : User Meta data Id                          : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/H ybridConnections/TestHybridConnection Name                        : TestHybridConnection Type                        : Microsoft.Relay/HybridConnections</span></span>

## <span data-ttu-id="0124b-129">筆記</span><span class="sxs-lookup"><span data-stu-id="0124b-129">NOTES</span></span>

## <span data-ttu-id="0124b-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="0124b-130">RELATED LINKS</span></span>

