---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: CEA14FAB-4B57-48F2-938C-E3AD4AAAE753
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/new-azurermservermanagementnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementNode.md
ms.openlocfilehash: 498be36141d1a44d33cdcb351b92d5b6908071c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444344"
---
# <span data-ttu-id="de4fd-101">New-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="de4fd-101">New-AzureRmServerManagementNode</span></span>

## <span data-ttu-id="de4fd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="de4fd-102">SYNOPSIS</span></span>
<span data-ttu-id="de4fd-103">建立 [伺服器管理] 節點。</span><span class="sxs-lookup"><span data-stu-id="de4fd-103">Creates a Server Management node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de4fd-104">句法</span><span class="sxs-lookup"><span data-stu-id="de4fd-104">SYNTAX</span></span>

### <span data-ttu-id="de4fd-105">ByName</span><span class="sxs-lookup"><span data-stu-id="de4fd-105">ByName</span></span>
```
New-AzureRmServerManagementNode [-ResourceGroupName] <String> [-GatewayName] <String> [-Location] <String>
 -NodeName <String> [-ComputerName <String>] -Credential <PSCredential> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de4fd-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="de4fd-106">ByObject</span></span>
```
New-AzureRmServerManagementNode [-Gateway] <Gateway> -NodeName <String> [-ComputerName <String>]
 -Credential <PSCredential> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de4fd-107">說明</span><span class="sxs-lookup"><span data-stu-id="de4fd-107">DESCRIPTION</span></span>
<span data-ttu-id="de4fd-108">**新的-AzureRmServerManagementNode** Cmdlet 會建立 Azure Server 管理節點。</span><span class="sxs-lookup"><span data-stu-id="de4fd-108">The **New-AzureRmServerManagementNode** cmdlet creates an Azure Server Management node.</span></span>

## <span data-ttu-id="de4fd-109">示例</span><span class="sxs-lookup"><span data-stu-id="de4fd-109">EXAMPLES</span></span>

## <span data-ttu-id="de4fd-110">參數</span><span class="sxs-lookup"><span data-stu-id="de4fd-110">PARAMETERS</span></span>

### <span data-ttu-id="de4fd-111">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="de4fd-111">-ComputerName</span></span>
<span data-ttu-id="de4fd-112">指定要管理之電腦的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="de4fd-112">Specifies the computer name of the computer that is being managed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de4fd-113">-認證</span><span class="sxs-lookup"><span data-stu-id="de4fd-113">-Credential</span></span>
<span data-ttu-id="de4fd-114">指定與伺服器管理節點連線的 **PSCredential** 物件。</span><span class="sxs-lookup"><span data-stu-id="de4fd-114">Specifies a **PSCredential** object for the connection to the Server Management Node.</span></span>
<span data-ttu-id="de4fd-115">若要取得認證物件，請使用 Get-Credential Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="de4fd-115">To obtain a credential object, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="de4fd-116">如需詳細資訊，請輸入 `Get-Help Get-Credential` 。</span><span class="sxs-lookup"><span data-stu-id="de4fd-116">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de4fd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de4fd-117">-DefaultProfile</span></span>
<span data-ttu-id="de4fd-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="de4fd-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de4fd-119">-閘道</span><span class="sxs-lookup"><span data-stu-id="de4fd-119">-Gateway</span></span>
<span data-ttu-id="de4fd-120">指定管理節點的閘道。</span><span class="sxs-lookup"><span data-stu-id="de4fd-120">Specifies the gateway that manages the node.</span></span>

<span data-ttu-id="de4fd-121">您可以使用這個參數，而不是 *ResourceGroupName* 、 *GatewayName* 和 *Location* 參數。</span><span class="sxs-lookup"><span data-stu-id="de4fd-121">This parameter can be used instead of the *ResourceGroupName* , *GatewayName* , and *Location* parameters.</span></span>

```yaml
Type: Gateway
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="de4fd-122">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="de4fd-122">-GatewayName</span></span>
<span data-ttu-id="de4fd-123">指定存取節點的閘道名稱。</span><span class="sxs-lookup"><span data-stu-id="de4fd-123">Specifies the name of the gateway that accesses the node.</span></span>

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

### <span data-ttu-id="de4fd-124">-位置</span><span class="sxs-lookup"><span data-stu-id="de4fd-124">-Location</span></span>
<span data-ttu-id="de4fd-125">指定此 Cmdlet 建立節點的位置。</span><span class="sxs-lookup"><span data-stu-id="de4fd-125">Specifies the location in which this cmdlet creates the node.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de4fd-126">-NodeName</span><span class="sxs-lookup"><span data-stu-id="de4fd-126">-NodeName</span></span>
<span data-ttu-id="de4fd-127">指定節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="de4fd-127">Specifies the name of the node.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de4fd-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de4fd-128">-ResourceGroupName</span></span>
<span data-ttu-id="de4fd-129">指定此 Cmdlet 在其中建立節點的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="de4fd-129">Specifies the name of the resource group in which this cmdlet creates the node.</span></span>

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

### <span data-ttu-id="de4fd-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="de4fd-130">-Tag</span></span>
<span data-ttu-id="de4fd-131">與物件相關聯的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="de4fd-131">Key/value pairs associated with the object.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de4fd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de4fd-132">CommonParameters</span></span>
<span data-ttu-id="de4fd-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="de4fd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de4fd-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="de4fd-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de4fd-135">輸入</span><span class="sxs-lookup"><span data-stu-id="de4fd-135">INPUTS</span></span>

### <span data-ttu-id="de4fd-136">關</span><span class="sxs-lookup"><span data-stu-id="de4fd-136">Gateway</span></span>
<span data-ttu-id="de4fd-137">參數 "閘道" 接受管線中 "Gateway" 類型的值</span><span class="sxs-lookup"><span data-stu-id="de4fd-137">Parameter 'Gateway' accepts value of type 'Gateway' from the pipeline</span></span>

## <span data-ttu-id="de4fd-138">輸出</span><span class="sxs-lookup"><span data-stu-id="de4fd-138">OUTPUTS</span></span>

### <span data-ttu-id="de4fd-139">[ServerManagement] 的節點</span><span class="sxs-lookup"><span data-stu-id="de4fd-139">Microsoft.Azure.Commands.ServerManagement.Model.Node</span></span>

## <span data-ttu-id="de4fd-140">筆記</span><span class="sxs-lookup"><span data-stu-id="de4fd-140">NOTES</span></span>

## <span data-ttu-id="de4fd-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="de4fd-141">RELATED LINKS</span></span>

[<span data-ttu-id="de4fd-142">AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="de4fd-142">Get-AzureRmServerManagementNode</span></span>](./Get-AzureRmServerManagementNode.md)

[<span data-ttu-id="de4fd-143">移除-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="de4fd-143">Remove-AzureRmServerManagementNode</span></span>](./Remove-AzureRmServerManagementNode.md)


