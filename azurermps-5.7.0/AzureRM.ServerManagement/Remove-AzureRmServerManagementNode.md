---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: B66C7A03-862A-497D-977B-1C43089DE24B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/remove-azurermservermanagementnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementNode.md
ms.openlocfilehash: 78fa17dee687547b617ff02dd11ecbf662e48040
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623586"
---
# <span data-ttu-id="45df0-101">Remove-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="45df0-101">Remove-AzureRmServerManagementNode</span></span>

## <span data-ttu-id="45df0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="45df0-102">SYNOPSIS</span></span>
<span data-ttu-id="45df0-103">移除 [伺服器管理] 節點。</span><span class="sxs-lookup"><span data-stu-id="45df0-103">Removes a Server Management node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45df0-104">句法</span><span class="sxs-lookup"><span data-stu-id="45df0-104">SYNTAX</span></span>

### <span data-ttu-id="45df0-105">ByName</span><span class="sxs-lookup"><span data-stu-id="45df0-105">ByName</span></span>
```
Remove-AzureRmServerManagementNode [-ResourceGroupName] <String> [-NodeName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45df0-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="45df0-106">ByObject</span></span>
```
Remove-AzureRmServerManagementNode [-Node] <Node> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="45df0-107">說明</span><span class="sxs-lookup"><span data-stu-id="45df0-107">DESCRIPTION</span></span>
<span data-ttu-id="45df0-108">**AzureRmServerManagementNode** Cmdlet 會移除 Azure Server 管理節點。</span><span class="sxs-lookup"><span data-stu-id="45df0-108">The **Remove-AzureRmServerManagementNode** cmdlet removes an Azure Server Management node.</span></span>

## <span data-ttu-id="45df0-109">示例</span><span class="sxs-lookup"><span data-stu-id="45df0-109">EXAMPLES</span></span>

## <span data-ttu-id="45df0-110">參數</span><span class="sxs-lookup"><span data-stu-id="45df0-110">PARAMETERS</span></span>

### <span data-ttu-id="45df0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45df0-111">-DefaultProfile</span></span>
<span data-ttu-id="45df0-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="45df0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45df0-113">-Node</span><span class="sxs-lookup"><span data-stu-id="45df0-113">-Node</span></span>
<span data-ttu-id="45df0-114">指定此 Cmdlet 移除的節點。</span><span class="sxs-lookup"><span data-stu-id="45df0-114">Specifies the node for which this cmdlet removes.</span></span>

<span data-ttu-id="45df0-115">您可以使用這個參數，而不是 *ResourceGroupName* 和 *NodeName* 參數。</span><span class="sxs-lookup"><span data-stu-id="45df0-115">This parameter may be used instead of the *ResourceGroupName* and *NodeName* parameters.</span></span>

```yaml
Type: Node
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="45df0-116">-NodeName</span><span class="sxs-lookup"><span data-stu-id="45df0-116">-NodeName</span></span>
<span data-ttu-id="45df0-117">指定此 Cmdlet 移除之節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="45df0-117">Specifies the name of the node for which this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45df0-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45df0-118">-ResourceGroupName</span></span>
<span data-ttu-id="45df0-119">指定節點所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="45df0-119">Specifies the name of the resource group that the node belongs to.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45df0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45df0-120">CommonParameters</span></span>
<span data-ttu-id="45df0-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="45df0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45df0-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="45df0-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45df0-123">輸入</span><span class="sxs-lookup"><span data-stu-id="45df0-123">INPUTS</span></span>

### <span data-ttu-id="45df0-124">節點</span><span class="sxs-lookup"><span data-stu-id="45df0-124">Node</span></span>
<span data-ttu-id="45df0-125">形參 "Node" 接受管線中 "Node" 類型的值</span><span class="sxs-lookup"><span data-stu-id="45df0-125">Parameter 'Node' accepts value of type 'Node' from the pipeline</span></span>

## <span data-ttu-id="45df0-126">輸出</span><span class="sxs-lookup"><span data-stu-id="45df0-126">OUTPUTS</span></span>

## <span data-ttu-id="45df0-127">筆記</span><span class="sxs-lookup"><span data-stu-id="45df0-127">NOTES</span></span>

## <span data-ttu-id="45df0-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="45df0-128">RELATED LINKS</span></span>

[<span data-ttu-id="45df0-129">AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="45df0-129">Get-AzureRmServerManagementNode</span></span>](./Get-AzureRmServerManagementNode.md)

[<span data-ttu-id="45df0-130">新-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="45df0-130">New-AzureRmServerManagementNode</span></span>](./New-AzureRmServerManagementNode.md)


