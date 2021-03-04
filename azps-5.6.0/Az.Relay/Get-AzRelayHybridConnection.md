---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/get-azrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayHybridConnection.md
ms.openlocfilehash: 9e7edf3a7aa076d7bb5ad4b1a36aecdedfd89b92
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914613"
---
# <span data-ttu-id="34755-101">Get-AzRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="34755-101">Get-AzRelayHybridConnection</span></span>

## <span data-ttu-id="34755-102">簡介</span><span class="sxs-lookup"><span data-stu-id="34755-102">SYNOPSIS</span></span>
<span data-ttu-id="34755-103">在 Relay 命名空間中，獲得指定 HybridConnection 的描述。</span><span class="sxs-lookup"><span data-stu-id="34755-103">Gets a description for the specified HybridConnection within the Relay namespace.</span></span>

## <span data-ttu-id="34755-104">語法</span><span class="sxs-lookup"><span data-stu-id="34755-104">SYNTAX</span></span>

```
Get-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34755-105">描述</span><span class="sxs-lookup"><span data-stu-id="34755-105">DESCRIPTION</span></span>
<span data-ttu-id="34755-106">**Get-AzRelayHybridConnection** Cmdlet 會取得 Relay 命名空間中指定混合連接的描述。</span><span class="sxs-lookup"><span data-stu-id="34755-106">The **Get-AzRelayHybridConnection** cmdlet gets a description for the specified HybridConnection within the Relay namespace.</span></span>

## <span data-ttu-id="34755-107">例子</span><span class="sxs-lookup"><span data-stu-id="34755-107">EXAMPLES</span></span>

### <span data-ttu-id="34755-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="34755-108">Example 1</span></span>
```
PS C:\>Get-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection

CreatedAt                   : 4/12/2017 3:17:02 AM
UpdatedAt                   : 4/12/2017 3:17:02 AM
ListenerCount               : 0
RequiresClientAuthorization : True
UserMetadata                : User Meta data
Id                          : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/H
                              ybridConnections/TestHybridConnection
Name                        : TestHybridConnection
Type                        : Microsoft.Relay/HybridConnections
```

<span data-ttu-id="34755-109">會返回 HybridConnection 的描述。</span><span class="sxs-lookup"><span data-stu-id="34755-109">Returns the description of the HybridConnection.</span></span>

## <span data-ttu-id="34755-110">參數</span><span class="sxs-lookup"><span data-stu-id="34755-110">PARAMETERS</span></span>

### <span data-ttu-id="34755-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34755-111">-DefaultProfile</span></span>
<span data-ttu-id="34755-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="34755-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34755-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="34755-113">-Name</span></span>
<span data-ttu-id="34755-114">HybridConnections Name.</span><span class="sxs-lookup"><span data-stu-id="34755-114">HybridConnections Name.</span></span>

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

### <span data-ttu-id="34755-115">-命名空間</span><span class="sxs-lookup"><span data-stu-id="34755-115">-Namespace</span></span>
<span data-ttu-id="34755-116">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="34755-116">Namespace Name.</span></span>

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

### <span data-ttu-id="34755-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34755-117">-ResourceGroupName</span></span>
<span data-ttu-id="34755-118">資源組名。</span><span class="sxs-lookup"><span data-stu-id="34755-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="34755-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34755-119">CommonParameters</span></span>
<span data-ttu-id="34755-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="34755-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34755-121">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="34755-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34755-122">輸入</span><span class="sxs-lookup"><span data-stu-id="34755-122">INPUTS</span></span>

### <span data-ttu-id="34755-123">System.String</span><span class="sxs-lookup"><span data-stu-id="34755-123">System.String</span></span>

## <span data-ttu-id="34755-124">輸出</span><span class="sxs-lookup"><span data-stu-id="34755-124">OUTPUTS</span></span>

### <span data-ttu-id="34755-125">Microsoft.Azure.Commands.Relay.models.PSHybridConnectionAttributes</span><span class="sxs-lookup"><span data-stu-id="34755-125">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span></span>

## <span data-ttu-id="34755-126">筆記</span><span class="sxs-lookup"><span data-stu-id="34755-126">NOTES</span></span>

## <span data-ttu-id="34755-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="34755-127">RELATED LINKS</span></span>
