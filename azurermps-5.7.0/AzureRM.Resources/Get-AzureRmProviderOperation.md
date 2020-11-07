---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6424B740-DBFB-490C-AEAA-EDD60952B435
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermprovideroperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderOperation.md
ms.openlocfilehash: 51229c966c0e4c8b0ec74c3c940037aca5081b15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625454"
---
# <span data-ttu-id="2c54f-101">Get-AzureRmProviderOperation</span><span class="sxs-lookup"><span data-stu-id="2c54f-101">Get-AzureRmProviderOperation</span></span>

## <span data-ttu-id="2c54f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2c54f-102">SYNOPSIS</span></span>
<span data-ttu-id="2c54f-103">取得使用 Azure RBAC 安全的 Azure 資源提供者的作業。</span><span class="sxs-lookup"><span data-stu-id="2c54f-103">Gets the operations for an Azure resource provider that are securable using Azure RBAC.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c54f-104">句法</span><span class="sxs-lookup"><span data-stu-id="2c54f-104">SYNTAX</span></span>

```
Get-AzureRmProviderOperation [[-OperationSearchString] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2c54f-105">說明</span><span class="sxs-lookup"><span data-stu-id="2c54f-105">DESCRIPTION</span></span>
<span data-ttu-id="2c54f-106">Get-AzureRmProviderOperation 會取得 Azure 資源提供者所公開的操作。</span><span class="sxs-lookup"><span data-stu-id="2c54f-106">The Get-AzureRmProviderOperation gets the operations exposed by Azure resource providers.</span></span>
<span data-ttu-id="2c54f-107">您可以撰寫作業來建立 Azure RBAC 中的自訂角色。</span><span class="sxs-lookup"><span data-stu-id="2c54f-107">Operations can be composed to create custom roles in Azure RBAC.</span></span>
<span data-ttu-id="2c54f-108">此命令會以輸入操作的方式， (中使用萬用字元 ( \* ) 字元 (s) # A5，決定要顯示的操作詳細資料。</span><span class="sxs-lookup"><span data-stu-id="2c54f-108">The command takes as input an operation search string (with possible wildcard(\*) character(s)) which determines the operations details to display.</span></span>

<span data-ttu-id="2c54f-109">使用 Get-AzureRmProviderOperation \* 來取得所有 Azure 資源提供者的所有作業。</span><span class="sxs-lookup"><span data-stu-id="2c54f-109">Use Get-AzureRmProviderOperation \* to get all operations for all Azure resource providers.</span></span>

<span data-ttu-id="2c54f-110">使用 Get-AzureRmProviderOperation 的 Microsoft. Compute/\* 來取得 Microsoft 的所有操作。計算資源提供者。</span><span class="sxs-lookup"><span data-stu-id="2c54f-110">Use Get-AzureRmProviderOperation Microsoft.Compute/\* to get all operations of Microsoft.Compute resource provider.</span></span>

## <span data-ttu-id="2c54f-111">示例</span><span class="sxs-lookup"><span data-stu-id="2c54f-111">EXAMPLES</span></span>

### <span data-ttu-id="2c54f-112">取得所有提供者的所有動作</span><span class="sxs-lookup"><span data-stu-id="2c54f-112">Get all actions for all providers</span></span>
```
PS C:\> Get-AzureRmProviderOperation *
```

### <span data-ttu-id="2c54f-113">針對特定資源提供者取得動作</span><span class="sxs-lookup"><span data-stu-id="2c54f-113">Get actions for a particular resource provider</span></span>
```
PS C:\> Get-AzureRmProviderOperation Microsoft.Insights/*
```

### <span data-ttu-id="2c54f-114">取得可在虛擬機器上執行的所有動作</span><span class="sxs-lookup"><span data-stu-id="2c54f-114">Get all actions that can be performed on virtual machines</span></span>
```
PS C:\> Get-AzureRmProviderOperation */virtualMachines/*
```

## <span data-ttu-id="2c54f-115">參數</span><span class="sxs-lookup"><span data-stu-id="2c54f-115">PARAMETERS</span></span>

### <span data-ttu-id="2c54f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c54f-116">-DefaultProfile</span></span>
<span data-ttu-id="2c54f-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="2c54f-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2c54f-118">-OperationSearchString</span><span class="sxs-lookup"><span data-stu-id="2c54f-118">-OperationSearchString</span></span>
<span data-ttu-id="2c54f-119">使用可能的萬用字元 ( \* ) 字元 (的操作搜尋字串) </span><span class="sxs-lookup"><span data-stu-id="2c54f-119">The operation search string (with possible wildcard (\*) characters)</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 0
Default value: "*"
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c54f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c54f-120">CommonParameters</span></span>
<span data-ttu-id="2c54f-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2c54f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c54f-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2c54f-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c54f-123">輸入</span><span class="sxs-lookup"><span data-stu-id="2c54f-123">INPUTS</span></span>

### <span data-ttu-id="2c54f-124">字串</span><span class="sxs-lookup"><span data-stu-id="2c54f-124">String</span></span>
<span data-ttu-id="2c54f-125">"OperationSearchString" 參數從管線接受類型 "String" 的值</span><span class="sxs-lookup"><span data-stu-id="2c54f-125">Parameter 'OperationSearchString' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="2c54f-126">輸出</span><span class="sxs-lookup"><span data-stu-id="2c54f-126">OUTPUTS</span></span>

### <span data-ttu-id="2c54f-127">PSResourceProviderOperation 中的 .Resources。</span><span class="sxs-lookup"><span data-stu-id="2c54f-127">Microsoft.Azure.Commands.Resources.Models.PSResourceProviderOperation</span></span>

## <span data-ttu-id="2c54f-128">筆記</span><span class="sxs-lookup"><span data-stu-id="2c54f-128">NOTES</span></span>
<span data-ttu-id="2c54f-129">關鍵字： azure，azurerm，arm，資源，管理，管理員，資源，群組，範本，部署</span><span class="sxs-lookup"><span data-stu-id="2c54f-129">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="2c54f-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="2c54f-130">RELATED LINKS</span></span>
