---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D5EB9AFA-B56C-45E2-838B-4555ED1EF8F8
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOperation.md
ms.openlocfilehash: 5807925c302f951f9e48c89afcb62634bd774c89
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917510"
---
# <span data-ttu-id="5894f-101">Get-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="5894f-101">Get-AzApiManagementOperation</span></span>

## <span data-ttu-id="5894f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5894f-102">SYNOPSIS</span></span>
<span data-ttu-id="5894f-103">獲得清單或指定的 API 運算。</span><span class="sxs-lookup"><span data-stu-id="5894f-103">Gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="5894f-104">語法</span><span class="sxs-lookup"><span data-stu-id="5894f-104">SYNTAX</span></span>

### <span data-ttu-id="5894f-105">GetAllApiOperations (預設) </span><span class="sxs-lookup"><span data-stu-id="5894f-105">GetAllApiOperations (Default)</span></span>
```
Get-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5894f-106">GetById</span><span class="sxs-lookup"><span data-stu-id="5894f-106">GetById</span></span>
```
Get-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5894f-107">描述</span><span class="sxs-lookup"><span data-stu-id="5894f-107">DESCRIPTION</span></span>
<span data-ttu-id="5894f-108">**Get-AzApiManagementOperation 會** 取得清單或指定的 API 運算。</span><span class="sxs-lookup"><span data-stu-id="5894f-108">The **Get-AzApiManagementOperation** gets a list or a specified API Operation.</span></span>

## <span data-ttu-id="5894f-109">例子</span><span class="sxs-lookup"><span data-stu-id="5894f-109">EXAMPLES</span></span>

### <span data-ttu-id="5894f-110">範例 1：取得所有 API 管理作業</span><span class="sxs-lookup"><span data-stu-id="5894f-110">Example 1: Get all API management operations</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOperation -Context $apimContext -ApiId $APIId
```

<span data-ttu-id="5894f-111">此命令會執行所有 API 管理作業。</span><span class="sxs-lookup"><span data-stu-id="5894f-111">This command gets all API management operations.</span></span>

### <span data-ttu-id="5894f-112">範例 2：根據作業識別碼取得 API 管理作業</span><span class="sxs-lookup"><span data-stu-id="5894f-112">Example 2: Get an API Management operation by operation ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "Operation003"
```

<span data-ttu-id="5894f-113">此命令會使用名為 Operation0003 的作業識別碼進行 API 管理作業。</span><span class="sxs-lookup"><span data-stu-id="5894f-113">This command gets an API management operation by operation ID named Operation0003.</span></span>

## <span data-ttu-id="5894f-114">參數</span><span class="sxs-lookup"><span data-stu-id="5894f-114">PARAMETERS</span></span>

### <span data-ttu-id="5894f-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="5894f-115">-ApiId</span></span>
<span data-ttu-id="5894f-116">指定 API 運算的識別碼。</span><span class="sxs-lookup"><span data-stu-id="5894f-116">Specifies the identifier of the API Operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5894f-117">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="5894f-117">-ApiRevision</span></span>
<span data-ttu-id="5894f-118">API 修訂的識別碼。</span><span class="sxs-lookup"><span data-stu-id="5894f-118">Identifier of API Revision.</span></span> <span data-ttu-id="5894f-119">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="5894f-119">This parameter is optional.</span></span> <span data-ttu-id="5894f-120">如果未指定，將會從目前使用中的 Api 修訂中取回作業。</span><span class="sxs-lookup"><span data-stu-id="5894f-120">If not specified, the operation will be retrieved from the currently active api revision.</span></span>

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

### <span data-ttu-id="5894f-121">-內容</span><span class="sxs-lookup"><span data-stu-id="5894f-121">-Context</span></span>
<span data-ttu-id="5894f-122">指定 **PsApiManagementCoNtext 物件** 的實例。</span><span class="sxs-lookup"><span data-stu-id="5894f-122">Specifies the instance of the **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5894f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5894f-123">-DefaultProfile</span></span>
<span data-ttu-id="5894f-124">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5894f-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5894f-125">-OperationId</span><span class="sxs-lookup"><span data-stu-id="5894f-125">-OperationId</span></span>
<span data-ttu-id="5894f-126">指定作業識別碼。</span><span class="sxs-lookup"><span data-stu-id="5894f-126">Specifies the operation identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5894f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5894f-127">CommonParameters</span></span>
<span data-ttu-id="5894f-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5894f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5894f-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5894f-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5894f-130">輸入</span><span class="sxs-lookup"><span data-stu-id="5894f-130">INPUTS</span></span>

### <span data-ttu-id="5894f-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="5894f-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5894f-132">System.String</span><span class="sxs-lookup"><span data-stu-id="5894f-132">System.String</span></span>

## <span data-ttu-id="5894f-133">輸出</span><span class="sxs-lookup"><span data-stu-id="5894f-133">OUTPUTS</span></span>

### <span data-ttu-id="5894f-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="5894f-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="5894f-135">筆記</span><span class="sxs-lookup"><span data-stu-id="5894f-135">NOTES</span></span>

## <span data-ttu-id="5894f-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="5894f-136">RELATED LINKS</span></span>

[<span data-ttu-id="5894f-137">New-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="5894f-137">New-AzApiManagementOperation</span></span>](./New-AzApiManagementOperation.md)

[<span data-ttu-id="5894f-138">Remove-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="5894f-138">Remove-AzApiManagementOperation</span></span>](./Remove-AzApiManagementOperation.md)

[<span data-ttu-id="5894f-139">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="5894f-139">Set-AzApiManagementOperation</span></span>](./Set-AzApiManagementOperation.md)


