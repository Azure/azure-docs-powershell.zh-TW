---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: 8942D757-B204-49CE-BCDE-68C3722913B3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementSession.md
ms.openlocfilehash: e3388a06a2835fcd9865a9aa46d376b693152bc8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449527"
---
# <span data-ttu-id="acb46-101">Get-AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="acb46-101">Get-AzureRmServerManagementSession</span></span>

## <span data-ttu-id="acb46-102">摘要</span><span class="sxs-lookup"><span data-stu-id="acb46-102">SYNOPSIS</span></span>
<span data-ttu-id="acb46-103">取得伺服器管理會話。</span><span class="sxs-lookup"><span data-stu-id="acb46-103">Gets a Server Management session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="acb46-104">句法</span><span class="sxs-lookup"><span data-stu-id="acb46-104">SYNTAX</span></span>

### <span data-ttu-id="acb46-105">ByNodeName</span><span class="sxs-lookup"><span data-stu-id="acb46-105">ByNodeName</span></span>
```
Get-AzureRmServerManagementSession [-ResourceGroupName] <String> [-NodeName] <String> [-SessionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="acb46-106">BySession</span><span class="sxs-lookup"><span data-stu-id="acb46-106">BySession</span></span>
```
Get-AzureRmServerManagementSession [[-SessionName] <String>] [-Session] <Session>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="acb46-107">ByNode</span><span class="sxs-lookup"><span data-stu-id="acb46-107">ByNode</span></span>
```
Get-AzureRmServerManagementSession [-Node] <Node> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="acb46-108">說明</span><span class="sxs-lookup"><span data-stu-id="acb46-108">DESCRIPTION</span></span>
<span data-ttu-id="acb46-109">**AzureRmServerManagementSession** Cmdlet 會取得單一 Azure 伺服器管理會話。</span><span class="sxs-lookup"><span data-stu-id="acb46-109">The **Get-AzureRmServerManagementSession** cmdlet gets a single Azure Server Management session.</span></span>

## <span data-ttu-id="acb46-110">示例</span><span class="sxs-lookup"><span data-stu-id="acb46-110">EXAMPLES</span></span>

## <span data-ttu-id="acb46-111">參數</span><span class="sxs-lookup"><span data-stu-id="acb46-111">PARAMETERS</span></span>

### <span data-ttu-id="acb46-112">-Node</span><span class="sxs-lookup"><span data-stu-id="acb46-112">-Node</span></span>
<span data-ttu-id="acb46-113">指定用於取得 *ResourceGroupName* 和 *NodeName* 參數的現有 **Node** 物件。</span><span class="sxs-lookup"><span data-stu-id="acb46-113">Specifies an existing **Node** object that is used to get the *ResourceGroupName* and the *NodeName* parameters.</span></span>
<span data-ttu-id="acb46-114">您也必須指定 *SessionName* 參數的值。</span><span class="sxs-lookup"><span data-stu-id="acb46-114">You must also specify a value for the *SessionName* parameter.</span></span>

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

### <span data-ttu-id="acb46-115">-NodeName</span><span class="sxs-lookup"><span data-stu-id="acb46-115">-NodeName</span></span>
<span data-ttu-id="acb46-116">指定會話所在之節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="acb46-116">Specifies the name of the node where the session is located.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNodeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acb46-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acb46-117">-ResourceGroupName</span></span>
<span data-ttu-id="acb46-118">指定此 Cmdlet 取得其檢索會話之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="acb46-118">Specifies the name of the resource group for which this cmdlet gets the retrieve the session.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNodeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acb46-119">-會話</span><span class="sxs-lookup"><span data-stu-id="acb46-119">-Session</span></span>
<span data-ttu-id="acb46-120">指定用於取得 *ResourceGroupName* 、 *NodeName* 及 *SessionName* 參數的現有 **會話** 物件。</span><span class="sxs-lookup"><span data-stu-id="acb46-120">Specifies an existing **Session** object that is used to get the *ResourceGroupName* , the *NodeName* , and the *SessionName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Session
Parameter Sets: BySession
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="acb46-121">-SessionName</span><span class="sxs-lookup"><span data-stu-id="acb46-121">-SessionName</span></span>
<span data-ttu-id="acb46-122">指定此 Cmdlet 所取得之會話的名稱。</span><span class="sxs-lookup"><span data-stu-id="acb46-122">Specifies the name of the session in which this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNodeName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: BySession
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acb46-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acb46-123">-DefaultProfile</span></span>
<span data-ttu-id="acb46-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="acb46-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="acb46-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acb46-125">CommonParameters</span></span>
<span data-ttu-id="acb46-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="acb46-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acb46-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="acb46-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acb46-128">輸入</span><span class="sxs-lookup"><span data-stu-id="acb46-128">INPUTS</span></span>

### <span data-ttu-id="acb46-129">節點</span><span class="sxs-lookup"><span data-stu-id="acb46-129">Node</span></span>
<span data-ttu-id="acb46-130">形參 "Node" 接受管線中 "Node" 類型的值</span><span class="sxs-lookup"><span data-stu-id="acb46-130">Parameter 'Node' accepts value of type 'Node' from the pipeline</span></span>

### <span data-ttu-id="acb46-131">課時</span><span class="sxs-lookup"><span data-stu-id="acb46-131">Session</span></span>
<span data-ttu-id="acb46-132">參數 "Session" 接受管線中類型 "Session" 的值</span><span class="sxs-lookup"><span data-stu-id="acb46-132">Parameter 'Session' accepts value of type 'Session' from the pipeline</span></span>

## <span data-ttu-id="acb46-133">輸出</span><span class="sxs-lookup"><span data-stu-id="acb46-133">OUTPUTS</span></span>

### <span data-ttu-id="acb46-134">[ServerManagement] 的課時</span><span class="sxs-lookup"><span data-stu-id="acb46-134">Microsoft.Azure.Commands.ServerManagement.Model.Session</span></span>

## <span data-ttu-id="acb46-135">筆記</span><span class="sxs-lookup"><span data-stu-id="acb46-135">NOTES</span></span>

## <span data-ttu-id="acb46-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="acb46-136">RELATED LINKS</span></span>

[<span data-ttu-id="acb46-137">Azure Server 管理 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="acb46-137">Azure Server Management Cmdlets</span></span>](./AzureRM.ServerManagement.md)


