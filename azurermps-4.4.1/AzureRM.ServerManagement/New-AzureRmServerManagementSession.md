---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: 5981D3D8-E2E7-4905-8CD0-8BDC35BB39AC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementSession.md
ms.openlocfilehash: 0ae3e221ee39a00381f009f45a9a2f508a552b6e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447998"
---
# <span data-ttu-id="9eebc-101">New-AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="9eebc-101">New-AzureRmServerManagementSession</span></span>

## <span data-ttu-id="9eebc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9eebc-102">SYNOPSIS</span></span>
<span data-ttu-id="9eebc-103">建立伺服器管理會話。</span><span class="sxs-lookup"><span data-stu-id="9eebc-103">Creates a Server Management session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9eebc-104">句法</span><span class="sxs-lookup"><span data-stu-id="9eebc-104">SYNTAX</span></span>

### <span data-ttu-id="9eebc-105">ByName</span><span class="sxs-lookup"><span data-stu-id="9eebc-105">ByName</span></span>
```
New-AzureRmServerManagementSession [-ResourceGroupName] <String> [-NodeName] <String> [-SessionName <String>]
 [-Credential <PSCredential>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9eebc-106">ByNode</span><span class="sxs-lookup"><span data-stu-id="9eebc-106">ByNode</span></span>
```
New-AzureRmServerManagementSession [-Node] <Node> [-SessionName <String>] [-Credential <PSCredential>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9eebc-107">說明</span><span class="sxs-lookup"><span data-stu-id="9eebc-107">DESCRIPTION</span></span>
<span data-ttu-id="9eebc-108">**新的-AzureRmServerManagementSession** Cmdlet 會建立 Azure Server 管理會話。</span><span class="sxs-lookup"><span data-stu-id="9eebc-108">The **New-AzureRmServerManagementSession** cmdlet creates an Azure Server Management session.</span></span>

## <span data-ttu-id="9eebc-109">示例</span><span class="sxs-lookup"><span data-stu-id="9eebc-109">EXAMPLES</span></span>

## <span data-ttu-id="9eebc-110">參數</span><span class="sxs-lookup"><span data-stu-id="9eebc-110">PARAMETERS</span></span>

### <span data-ttu-id="9eebc-111">-認證</span><span class="sxs-lookup"><span data-stu-id="9eebc-111">-Credential</span></span>
<span data-ttu-id="9eebc-112">指定與伺服器管理會話連線的 **PSCredential** 物件。</span><span class="sxs-lookup"><span data-stu-id="9eebc-112">Specifies a **PSCredential** object for the connection to the Server Management Session.</span></span>
<span data-ttu-id="9eebc-113">若要取得認證物件，請使用 Get-Credential Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9eebc-113">To obtain a credential object, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="9eebc-114">如需詳細資訊，請輸入 `Get-Help Get-Credential` 。</span><span class="sxs-lookup"><span data-stu-id="9eebc-114">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9eebc-115">-Node</span><span class="sxs-lookup"><span data-stu-id="9eebc-115">-Node</span></span>
<span data-ttu-id="9eebc-116">指定此 Cmdlet 在其上建立會話的節點。</span><span class="sxs-lookup"><span data-stu-id="9eebc-116">Specifies the node for which this cmdlet creates the session on.</span></span>

<span data-ttu-id="9eebc-117">您可以使用這個參數，而不是 *ResourceGroupName* 和 *NodeName* 參數。</span><span class="sxs-lookup"><span data-stu-id="9eebc-117">This parameter may be used instead of the *ResourceGroupName* and *NodeName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Node
Parameter Sets: ByNode
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9eebc-118">-NodeName</span><span class="sxs-lookup"><span data-stu-id="9eebc-118">-NodeName</span></span>
<span data-ttu-id="9eebc-119">指定此 Cmdlet 建立會話之節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="9eebc-119">Specifies the name of the node for which this cmdlet creates a session.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9eebc-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9eebc-120">-ResourceGroupName</span></span>
<span data-ttu-id="9eebc-121">指定此 Cmdlet 為其建立會話之節點的資源群組。</span><span class="sxs-lookup"><span data-stu-id="9eebc-121">Specifies the resource group of the node that this cmdlet creates a session for.</span></span>

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

### <span data-ttu-id="9eebc-122">-SessionName</span><span class="sxs-lookup"><span data-stu-id="9eebc-122">-SessionName</span></span>
<span data-ttu-id="9eebc-123">指定會話要使用的名稱。</span><span class="sxs-lookup"><span data-stu-id="9eebc-123">Specifies the name to use for the session.</span></span>

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

### <span data-ttu-id="9eebc-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9eebc-124">-DefaultProfile</span></span>
<span data-ttu-id="9eebc-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9eebc-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9eebc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9eebc-126">CommonParameters</span></span>
<span data-ttu-id="9eebc-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9eebc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9eebc-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9eebc-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9eebc-129">輸入</span><span class="sxs-lookup"><span data-stu-id="9eebc-129">INPUTS</span></span>

### <span data-ttu-id="9eebc-130">節點</span><span class="sxs-lookup"><span data-stu-id="9eebc-130">Node</span></span>
<span data-ttu-id="9eebc-131">形參 "Node" 接受管線中 "Node" 類型的值</span><span class="sxs-lookup"><span data-stu-id="9eebc-131">Parameter 'Node' accepts value of type 'Node' from the pipeline</span></span>

## <span data-ttu-id="9eebc-132">輸出</span><span class="sxs-lookup"><span data-stu-id="9eebc-132">OUTPUTS</span></span>

### <span data-ttu-id="9eebc-133">[ServerManagement] 的課時</span><span class="sxs-lookup"><span data-stu-id="9eebc-133">Microsoft.Azure.Commands.ServerManagement.Model.Session</span></span>

## <span data-ttu-id="9eebc-134">筆記</span><span class="sxs-lookup"><span data-stu-id="9eebc-134">NOTES</span></span>

## <span data-ttu-id="9eebc-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="9eebc-135">RELATED LINKS</span></span>

