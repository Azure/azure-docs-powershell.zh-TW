---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 2FD2C5C0-5A5A-4CF0-9260-21B9E3DE52B9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementproductfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProductFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProductFromGroup.md
ms.openlocfilehash: 2eba88e94cfed3c253a5b5febc20a7585ab096d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444819"
---
# <span data-ttu-id="a72bf-101">Remove-AzureRmApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="a72bf-101">Remove-AzureRmApiManagementProductFromGroup</span></span>

## <span data-ttu-id="a72bf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a72bf-102">SYNOPSIS</span></span>
<span data-ttu-id="a72bf-103">從群組中移除產品。</span><span class="sxs-lookup"><span data-stu-id="a72bf-103">Removes a product from a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a72bf-104">句法</span><span class="sxs-lookup"><span data-stu-id="a72bf-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementProductFromGroup -Context <PsApiManagementContext> -GroupId <String>
 -ProductId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a72bf-105">說明</span><span class="sxs-lookup"><span data-stu-id="a72bf-105">DESCRIPTION</span></span>
<span data-ttu-id="a72bf-106">**AzureRmApiManagementProductFromGroup** Cmdlet 會從現有的群組中移除產品。</span><span class="sxs-lookup"><span data-stu-id="a72bf-106">The **Remove-AzureRmApiManagementProductFromGroup** cmdlet removes a product from an existing group.</span></span>
<span data-ttu-id="a72bf-107">換句話說，這個 Cmdlet 會將群組指派從產品中移除。</span><span class="sxs-lookup"><span data-stu-id="a72bf-107">In other words, this cmdlet removes the group assignment from a product.</span></span>

## <span data-ttu-id="a72bf-108">示例</span><span class="sxs-lookup"><span data-stu-id="a72bf-108">EXAMPLES</span></span>

### <span data-ttu-id="a72bf-109">範例1：從群組中移除產品</span><span class="sxs-lookup"><span data-stu-id="a72bf-109">Example 1: Remove a product from a group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementProductFromGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="a72bf-110">這個命令會從現有的群組中移除產品。</span><span class="sxs-lookup"><span data-stu-id="a72bf-110">This command removes a product from an existing group.</span></span>

## <span data-ttu-id="a72bf-111">參數</span><span class="sxs-lookup"><span data-stu-id="a72bf-111">PARAMETERS</span></span>

### <span data-ttu-id="a72bf-112">-內容</span><span class="sxs-lookup"><span data-stu-id="a72bf-112">-Context</span></span>
<span data-ttu-id="a72bf-113">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="a72bf-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="a72bf-114">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="a72bf-114">This parameter is required.</span></span>

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

### <span data-ttu-id="a72bf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a72bf-115">-DefaultProfile</span></span>
<span data-ttu-id="a72bf-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a72bf-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="a72bf-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="a72bf-117">-GroupId</span></span>
<span data-ttu-id="a72bf-118">指定群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="a72bf-118">Specifies the group ID.</span></span>
<span data-ttu-id="a72bf-119">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="a72bf-119">This parameter is required.</span></span>

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

### <span data-ttu-id="a72bf-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a72bf-120">-PassThru</span></span>
<span data-ttu-id="a72bf-121">指出這個 Cmdlet 會傳回 $True 的值（如果它成功的話），否則傳回 $False。</span><span class="sxs-lookup"><span data-stu-id="a72bf-121">Indicates that this cmdlet returns a value of $True, if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="a72bf-122">-產品識別碼</span><span class="sxs-lookup"><span data-stu-id="a72bf-122">-ProductId</span></span>
<span data-ttu-id="a72bf-123">指定產品識別碼。</span><span class="sxs-lookup"><span data-stu-id="a72bf-123">Specifies the product ID.</span></span>
<span data-ttu-id="a72bf-124">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="a72bf-124">This parameter is required.</span></span>

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

### <span data-ttu-id="a72bf-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a72bf-125">CommonParameters</span></span>
<span data-ttu-id="a72bf-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a72bf-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a72bf-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a72bf-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a72bf-128">輸入</span><span class="sxs-lookup"><span data-stu-id="a72bf-128">INPUTS</span></span>

### <span data-ttu-id="a72bf-129">所有</span><span class="sxs-lookup"><span data-stu-id="a72bf-129">None</span></span>
<span data-ttu-id="a72bf-130">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="a72bf-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a72bf-131">輸出</span><span class="sxs-lookup"><span data-stu-id="a72bf-131">OUTPUTS</span></span>

### <span data-ttu-id="a72bf-132">System.object</span><span class="sxs-lookup"><span data-stu-id="a72bf-132">System.Boolean</span></span>

## <span data-ttu-id="a72bf-133">筆記</span><span class="sxs-lookup"><span data-stu-id="a72bf-133">NOTES</span></span>

## <span data-ttu-id="a72bf-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="a72bf-134">RELATED LINKS</span></span>

[<span data-ttu-id="a72bf-135">附加 AzureRmApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="a72bf-135">Add-AzureRmApiManagementProductToGroup</span></span>](./Add-AzureRmApiManagementProductToGroup.md)


