---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: 4EE30890-B09B-4811-88AD-4BF4FD47E431
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/get-azurermservermanagementnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementNode.md
ms.openlocfilehash: f33c6b4c7ac1fc0f1b7de11afc8395232c599539
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447662"
---
# <span data-ttu-id="b5389-101">Get-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="b5389-101">Get-AzureRmServerManagementNode</span></span>

## <span data-ttu-id="b5389-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b5389-102">SYNOPSIS</span></span>
<span data-ttu-id="b5389-103">取得一或多個伺服器管理節點。</span><span class="sxs-lookup"><span data-stu-id="b5389-103">Gets one or more Server Management nodes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5389-104">句法</span><span class="sxs-lookup"><span data-stu-id="b5389-104">SYNTAX</span></span>

### <span data-ttu-id="b5389-105">ByNodeName</span><span class="sxs-lookup"><span data-stu-id="b5389-105">ByNodeName</span></span>
```
Get-AzureRmServerManagementNode [[-ResourceGroupName] <String>] [[-NodeName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5389-106">ByNode</span><span class="sxs-lookup"><span data-stu-id="b5389-106">ByNode</span></span>
```
Get-AzureRmServerManagementNode [-Node] <Node> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5389-107">說明</span><span class="sxs-lookup"><span data-stu-id="b5389-107">DESCRIPTION</span></span>
<span data-ttu-id="b5389-108">**AzureRmServerManagementNode** Cmdlet 會取得一或多個 Azure 伺服器管理節點。</span><span class="sxs-lookup"><span data-stu-id="b5389-108">The **Get-AzureRmServerManagementNode** cmdlet gets one or more Azure Server Management nodes.</span></span>

## <span data-ttu-id="b5389-109">示例</span><span class="sxs-lookup"><span data-stu-id="b5389-109">EXAMPLES</span></span>

## <span data-ttu-id="b5389-110">參數</span><span class="sxs-lookup"><span data-stu-id="b5389-110">PARAMETERS</span></span>

### <span data-ttu-id="b5389-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5389-111">-DefaultProfile</span></span>
<span data-ttu-id="b5389-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b5389-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5389-113">-Node</span><span class="sxs-lookup"><span data-stu-id="b5389-113">-Node</span></span>
<span data-ttu-id="b5389-114">指定要取得 *ResourceGroupName* 和 *NodeName* 參數的現有節點。</span><span class="sxs-lookup"><span data-stu-id="b5389-114">Specifies an existing node from which to get the *ResourceGroupName* and the *NodeName* parameters.</span></span>

```yaml
Type: Node
Parameter Sets: ByNode
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5389-115">-NodeName</span><span class="sxs-lookup"><span data-stu-id="b5389-115">-NodeName</span></span>
<span data-ttu-id="b5389-116">指定此 Cmdlet 取得之節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="b5389-116">Specifies the name of the node for which this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByNodeName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5389-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5389-117">-ResourceGroupName</span></span>
<span data-ttu-id="b5389-118">指定節點所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b5389-118">Specifies the name of the resource group in which the nodes belong to.</span></span>

```yaml
Type: String
Parameter Sets: ByNodeName
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5389-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5389-119">CommonParameters</span></span>
<span data-ttu-id="b5389-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b5389-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5389-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b5389-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5389-122">輸入</span><span class="sxs-lookup"><span data-stu-id="b5389-122">INPUTS</span></span>

### <span data-ttu-id="b5389-123">節點</span><span class="sxs-lookup"><span data-stu-id="b5389-123">Node</span></span>
<span data-ttu-id="b5389-124">形參 "Node" 接受管線中 "Node" 類型的值</span><span class="sxs-lookup"><span data-stu-id="b5389-124">Parameter 'Node' accepts value of type 'Node' from the pipeline</span></span>

## <span data-ttu-id="b5389-125">輸出</span><span class="sxs-lookup"><span data-stu-id="b5389-125">OUTPUTS</span></span>

### <span data-ttu-id="b5389-126">[ServerManagement] 的節點</span><span class="sxs-lookup"><span data-stu-id="b5389-126">Microsoft.Azure.Commands.ServerManagement.Model.Node</span></span>

## <span data-ttu-id="b5389-127">筆記</span><span class="sxs-lookup"><span data-stu-id="b5389-127">NOTES</span></span>

## <span data-ttu-id="b5389-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="b5389-128">RELATED LINKS</span></span>

[<span data-ttu-id="b5389-129">新-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="b5389-129">New-AzureRmServerManagementNode</span></span>](./New-AzureRmServerManagementNode.md)

[<span data-ttu-id="b5389-130">移除-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="b5389-130">Remove-AzureRmServerManagementNode</span></span>](./Remove-AzureRmServerManagementNode.md)


