---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: B66C7A03-862A-497D-977B-1C43089DE24B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementNode.md
ms.openlocfilehash: 93efff5a9f317b7d44d071a4dd212d235df02223
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449513"
---
# <span data-ttu-id="b12ef-101">Remove-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="b12ef-101">Remove-AzureRmServerManagementNode</span></span>

## <span data-ttu-id="b12ef-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b12ef-102">SYNOPSIS</span></span>
<span data-ttu-id="b12ef-103">移除 [伺服器管理] 節點。</span><span class="sxs-lookup"><span data-stu-id="b12ef-103">Removes a Server Management node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b12ef-104">句法</span><span class="sxs-lookup"><span data-stu-id="b12ef-104">SYNTAX</span></span>

### <span data-ttu-id="b12ef-105">ByName</span><span class="sxs-lookup"><span data-stu-id="b12ef-105">ByName</span></span>
```
Remove-AzureRmServerManagementNode [-ResourceGroupName] <String> [-NodeName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b12ef-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="b12ef-106">ByObject</span></span>
```
Remove-AzureRmServerManagementNode [-Node] <Node> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b12ef-107">說明</span><span class="sxs-lookup"><span data-stu-id="b12ef-107">DESCRIPTION</span></span>
<span data-ttu-id="b12ef-108">**AzureRmServerManagementNode** Cmdlet 會移除 Azure Server 管理節點。</span><span class="sxs-lookup"><span data-stu-id="b12ef-108">The **Remove-AzureRmServerManagementNode** cmdlet removes an Azure Server Management node.</span></span>

## <span data-ttu-id="b12ef-109">示例</span><span class="sxs-lookup"><span data-stu-id="b12ef-109">EXAMPLES</span></span>

## <span data-ttu-id="b12ef-110">參數</span><span class="sxs-lookup"><span data-stu-id="b12ef-110">PARAMETERS</span></span>

### <span data-ttu-id="b12ef-111">-Node</span><span class="sxs-lookup"><span data-stu-id="b12ef-111">-Node</span></span>
<span data-ttu-id="b12ef-112">指定此 Cmdlet 移除的節點。</span><span class="sxs-lookup"><span data-stu-id="b12ef-112">Specifies the node for which this cmdlet removes.</span></span>

<span data-ttu-id="b12ef-113">您可以使用這個參數，而不是 *ResourceGroupName* 和 *NodeName* 參數。</span><span class="sxs-lookup"><span data-stu-id="b12ef-113">This parameter may be used instead of the *ResourceGroupName* and *NodeName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Node
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b12ef-114">-NodeName</span><span class="sxs-lookup"><span data-stu-id="b12ef-114">-NodeName</span></span>
<span data-ttu-id="b12ef-115">指定此 Cmdlet 移除之節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="b12ef-115">Specifies the name of the node for which this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b12ef-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b12ef-116">-ResourceGroupName</span></span>
<span data-ttu-id="b12ef-117">指定節點所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b12ef-117">Specifies the name of the resource group that the node belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b12ef-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b12ef-118">-DefaultProfile</span></span>
<span data-ttu-id="b12ef-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b12ef-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b12ef-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b12ef-120">CommonParameters</span></span>
<span data-ttu-id="b12ef-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b12ef-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b12ef-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b12ef-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b12ef-123">輸入</span><span class="sxs-lookup"><span data-stu-id="b12ef-123">INPUTS</span></span>

### <span data-ttu-id="b12ef-124">節點</span><span class="sxs-lookup"><span data-stu-id="b12ef-124">Node</span></span>
<span data-ttu-id="b12ef-125">形參 "Node" 接受管線中 "Node" 類型的值</span><span class="sxs-lookup"><span data-stu-id="b12ef-125">Parameter 'Node' accepts value of type 'Node' from the pipeline</span></span>

## <span data-ttu-id="b12ef-126">輸出</span><span class="sxs-lookup"><span data-stu-id="b12ef-126">OUTPUTS</span></span>

## <span data-ttu-id="b12ef-127">筆記</span><span class="sxs-lookup"><span data-stu-id="b12ef-127">NOTES</span></span>

## <span data-ttu-id="b12ef-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="b12ef-128">RELATED LINKS</span></span>

[<span data-ttu-id="b12ef-129">AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="b12ef-129">Get-AzureRmServerManagementNode</span></span>](./Get-AzureRmServerManagementNode.md)

[<span data-ttu-id="b12ef-130">新-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="b12ef-130">New-AzureRmServerManagementNode</span></span>](./New-AzureRmServerManagementNode.md)


