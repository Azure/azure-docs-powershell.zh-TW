---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D5EB9AFA-B56C-45E2-838B-4555ED1EF8F8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOperation.md
ms.openlocfilehash: 1b1547485a4758764cf02eaca4fd7bc26d4ef990
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453228"
---
# <span data-ttu-id="5a75e-101">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="5a75e-101">Get-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="5a75e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5a75e-102">SYNOPSIS</span></span>
<span data-ttu-id="5a75e-103">取得清單或指定的 API 操作。</span><span class="sxs-lookup"><span data-stu-id="5a75e-103">Gets a list or a specified API Operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a75e-104">句法</span><span class="sxs-lookup"><span data-stu-id="5a75e-104">SYNTAX</span></span>

### <span data-ttu-id="5a75e-105">GetAllApiOperations (預設) </span><span class="sxs-lookup"><span data-stu-id="5a75e-105">GetAllApiOperations (Default)</span></span>
```
Get-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a75e-106">GetById</span><span class="sxs-lookup"><span data-stu-id="5a75e-106">GetById</span></span>
```
Get-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a75e-107">說明</span><span class="sxs-lookup"><span data-stu-id="5a75e-107">DESCRIPTION</span></span>
<span data-ttu-id="5a75e-108">**AzureRmApiManagementOperation** 會取得清單或指定的 API 操作。</span><span class="sxs-lookup"><span data-stu-id="5a75e-108">The **Get-AzureRmApiManagementOperation** gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="5a75e-109">示例</span><span class="sxs-lookup"><span data-stu-id="5a75e-109">EXAMPLES</span></span>

### <span data-ttu-id="5a75e-110">範例1：取得所有 API 管理作業</span><span class="sxs-lookup"><span data-stu-id="5a75e-110">Example 1: Get all API management operations</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOperation -Context $apimContext -ApiId $APIId
```

<span data-ttu-id="5a75e-111">這個命令會取得所有 API 管理作業。</span><span class="sxs-lookup"><span data-stu-id="5a75e-111">This command gets all API management operations.</span></span>

### <span data-ttu-id="5a75e-112">範例2：依作業 ID 取得 API 管理作業</span><span class="sxs-lookup"><span data-stu-id="5a75e-112">Example 2: Get an API Management operation by operation ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "Operation003"
```

<span data-ttu-id="5a75e-113">這個命令會透過名為 Operation0003 的操作 ID 取得 API 管理作業。</span><span class="sxs-lookup"><span data-stu-id="5a75e-113">This command gets an API management operation by operation ID named Operation0003.</span></span>

## <span data-ttu-id="5a75e-114">參數</span><span class="sxs-lookup"><span data-stu-id="5a75e-114">PARAMETERS</span></span>

### <span data-ttu-id="5a75e-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="5a75e-115">-ApiId</span></span>
<span data-ttu-id="5a75e-116">指定 API 操作的識別碼。</span><span class="sxs-lookup"><span data-stu-id="5a75e-116">Specifies the identifier of the API Operation.</span></span>

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

### <span data-ttu-id="5a75e-117">-內容</span><span class="sxs-lookup"><span data-stu-id="5a75e-117">-Context</span></span>
<span data-ttu-id="5a75e-118">指定 **PsApiManagementCoNtext** 物件的實例。</span><span class="sxs-lookup"><span data-stu-id="5a75e-118">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="5a75e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a75e-119">-DefaultProfile</span></span>
<span data-ttu-id="5a75e-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5a75e-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="5a75e-121">-OperationId</span><span class="sxs-lookup"><span data-stu-id="5a75e-121">-OperationId</span></span>
<span data-ttu-id="5a75e-122">指定操作識別碼。</span><span class="sxs-lookup"><span data-stu-id="5a75e-122">Specifies the operation identifier.</span></span>

```yaml
Type: String
Parameter Sets: GetById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a75e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a75e-123">CommonParameters</span></span>
<span data-ttu-id="5a75e-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5a75e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a75e-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5a75e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a75e-126">輸入</span><span class="sxs-lookup"><span data-stu-id="5a75e-126">INPUTS</span></span>

### <span data-ttu-id="5a75e-127">所有</span><span class="sxs-lookup"><span data-stu-id="5a75e-127">None</span></span>
<span data-ttu-id="5a75e-128">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="5a75e-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5a75e-129">輸出</span><span class="sxs-lookup"><span data-stu-id="5a75e-129">OUTPUTS</span></span>

### <span data-ttu-id="5a75e-130">ServiceManagement. PsApiManagementOperation （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="5a75e-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>
<span data-ttu-id="5a75e-131">Api 管理服務中 API 操作的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="5a75e-131">The details of the API Operation in Api Management service.</span></span>

### <span data-ttu-id="5a75e-132">IList<ApiManagement. ServiceManagement. PsApiManagementOperation]></span><span class="sxs-lookup"><span data-stu-id="5a75e-132">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation></span></span>
<span data-ttu-id="5a75e-133">Api 管理服務中的 API 動作清單。</span><span class="sxs-lookup"><span data-stu-id="5a75e-133">The list of API Operation in Api Management service.</span></span>

## <span data-ttu-id="5a75e-134">筆記</span><span class="sxs-lookup"><span data-stu-id="5a75e-134">NOTES</span></span>

## <span data-ttu-id="5a75e-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="5a75e-135">RELATED LINKS</span></span>

[<span data-ttu-id="5a75e-136">新-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="5a75e-136">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="5a75e-137">移除-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="5a75e-137">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)

[<span data-ttu-id="5a75e-138">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="5a75e-138">Set-AzureRmApiManagementOperation</span></span>](./Set-AzureRmApiManagementOperation.md)


