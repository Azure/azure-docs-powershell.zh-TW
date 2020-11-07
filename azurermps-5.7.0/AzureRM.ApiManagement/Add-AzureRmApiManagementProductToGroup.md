---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 1058BA4E-CD79-429D-BB05-422AE39230C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/add-azurermapimanagementproducttogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementProductToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementProductToGroup.md
ms.openlocfilehash: f7c1db6b4ce7c9df63506cdba8b1a206c22ee03e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626454"
---
# <span data-ttu-id="f09b5-101">Add-AzureRmApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="f09b5-101">Add-AzureRmApiManagementProductToGroup</span></span>

## <span data-ttu-id="f09b5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f09b5-102">SYNOPSIS</span></span>
<span data-ttu-id="f09b5-103">在群組中新增產品。</span><span class="sxs-lookup"><span data-stu-id="f09b5-103">Adds a product to a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f09b5-104">句法</span><span class="sxs-lookup"><span data-stu-id="f09b5-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementProductToGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f09b5-105">說明</span><span class="sxs-lookup"><span data-stu-id="f09b5-105">DESCRIPTION</span></span>
<span data-ttu-id="f09b5-106">**載入 AzureRmApiManagementProductToGroup** Cmdlet 會將產品新增至現有的群組。</span><span class="sxs-lookup"><span data-stu-id="f09b5-106">The **Add-AzureRmApiManagementProductToGroup** cmdlet adds a product to an existing group.</span></span>
<span data-ttu-id="f09b5-107">換句話說，這個 Cmdlet 會將群組指派給產品。</span><span class="sxs-lookup"><span data-stu-id="f09b5-107">In other words, this cmdlet assigns a group to a product.</span></span>

## <span data-ttu-id="f09b5-108">示例</span><span class="sxs-lookup"><span data-stu-id="f09b5-108">EXAMPLES</span></span>

### <span data-ttu-id="f09b5-109">範例1：將產品新增至群組</span><span class="sxs-lookup"><span data-stu-id="f09b5-109">Example 1: Add a product to a group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzureRmApiManagementProductToGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="f09b5-110">這個命令會將產品新增至現有的群組。</span><span class="sxs-lookup"><span data-stu-id="f09b5-110">This command adds a product to an existing group.</span></span>

## <span data-ttu-id="f09b5-111">參數</span><span class="sxs-lookup"><span data-stu-id="f09b5-111">PARAMETERS</span></span>

### <span data-ttu-id="f09b5-112">-內容</span><span class="sxs-lookup"><span data-stu-id="f09b5-112">-Context</span></span>
<span data-ttu-id="f09b5-113">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="f09b5-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="f09b5-114">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="f09b5-114">This parameter is required.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f09b5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f09b5-115">-DefaultProfile</span></span>
<span data-ttu-id="f09b5-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f09b5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="f09b5-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="f09b5-117">-GroupId</span></span>
<span data-ttu-id="f09b5-118">指定群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="f09b5-118">Specifies the group ID.</span></span>
<span data-ttu-id="f09b5-119">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="f09b5-119">This parameter is required.</span></span>

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

### <span data-ttu-id="f09b5-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f09b5-120">-PassThru</span></span>
<span data-ttu-id="f09b5-121">passthru</span><span class="sxs-lookup"><span data-stu-id="f09b5-121">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f09b5-122">-產品識別碼</span><span class="sxs-lookup"><span data-stu-id="f09b5-122">-ProductId</span></span>
<span data-ttu-id="f09b5-123">指定產品識別碼。</span><span class="sxs-lookup"><span data-stu-id="f09b5-123">Specifies the product ID.</span></span>
<span data-ttu-id="f09b5-124">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="f09b5-124">This parameter is required.</span></span>

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

### <span data-ttu-id="f09b5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f09b5-125">CommonParameters</span></span>
<span data-ttu-id="f09b5-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f09b5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f09b5-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f09b5-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f09b5-128">輸入</span><span class="sxs-lookup"><span data-stu-id="f09b5-128">INPUTS</span></span>

### <span data-ttu-id="f09b5-129">所有</span><span class="sxs-lookup"><span data-stu-id="f09b5-129">None</span></span>
<span data-ttu-id="f09b5-130">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="f09b5-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f09b5-131">輸出</span><span class="sxs-lookup"><span data-stu-id="f09b5-131">OUTPUTS</span></span>

### <span data-ttu-id="f09b5-132">布林值</span><span class="sxs-lookup"><span data-stu-id="f09b5-132">Boolean</span></span>

## <span data-ttu-id="f09b5-133">筆記</span><span class="sxs-lookup"><span data-stu-id="f09b5-133">NOTES</span></span>

## <span data-ttu-id="f09b5-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="f09b5-134">RELATED LINKS</span></span>

[<span data-ttu-id="f09b5-135">移除-AzureRmApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="f09b5-135">Remove-AzureRmApiManagementProductFromGroup</span></span>](./Remove-AzureRmApiManagementProductFromGroup.md)


