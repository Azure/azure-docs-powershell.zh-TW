---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2457C7F5-7FB9-4712-AD7C-438E88F591A8
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementapifromproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromProduct.md
ms.openlocfilehash: af83bb3d6daa11eb62de81378e4e7d3e040b2db4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903685"
---
# <span data-ttu-id="9169c-101">Remove-AzApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="9169c-101">Remove-AzApiManagementApiFromProduct</span></span>

## <span data-ttu-id="9169c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9169c-102">SYNOPSIS</span></span>
<span data-ttu-id="9169c-103">從產品移除 API。</span><span class="sxs-lookup"><span data-stu-id="9169c-103">Removes an API from a product.</span></span>

## <span data-ttu-id="9169c-104">語法</span><span class="sxs-lookup"><span data-stu-id="9169c-104">SYNTAX</span></span>

```
Remove-AzApiManagementApiFromProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9169c-105">描述</span><span class="sxs-lookup"><span data-stu-id="9169c-105">DESCRIPTION</span></span>
<span data-ttu-id="9169c-106">**Remove-AzApiManagementApiFromProduct** Cmdlet 會從產品移除 Azure API 管理 API。</span><span class="sxs-lookup"><span data-stu-id="9169c-106">The **Remove-AzApiManagementApiFromProduct** cmdlet removes an Azure API Management API from a product.</span></span>

## <span data-ttu-id="9169c-107">例子</span><span class="sxs-lookup"><span data-stu-id="9169c-107">EXAMPLES</span></span>

### <span data-ttu-id="9169c-108">範例 1：從產品移除 API</span><span class="sxs-lookup"><span data-stu-id="9169c-108">Example 1: Remove an API from a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiFromProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001" -PassThru
```

<span data-ttu-id="9169c-109">此命令會從產品移除指定的 API。</span><span class="sxs-lookup"><span data-stu-id="9169c-109">This command removes the specified API from a product.</span></span>

## <span data-ttu-id="9169c-110">參數</span><span class="sxs-lookup"><span data-stu-id="9169c-110">PARAMETERS</span></span>

### <span data-ttu-id="9169c-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="9169c-111">-ApiId</span></span>
<span data-ttu-id="9169c-112">指定要從產品移除的 API 識別碼。</span><span class="sxs-lookup"><span data-stu-id="9169c-112">Specifies the ID of the API to remove from the product.</span></span>

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

### <span data-ttu-id="9169c-113">-內容</span><span class="sxs-lookup"><span data-stu-id="9169c-113">-Context</span></span>
<span data-ttu-id="9169c-114">指定 **PsApiManagementCoNtext。**</span><span class="sxs-lookup"><span data-stu-id="9169c-114">Specifies a **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="9169c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9169c-115">-DefaultProfile</span></span>
<span data-ttu-id="9169c-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9169c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9169c-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9169c-117">-PassThru</span></span>
<span data-ttu-id="9169c-118">表示此 Cmdlet 會成功時$True值，否則會$False值。</span><span class="sxs-lookup"><span data-stu-id="9169c-118">Indicates that this cmdlet returns a value of $True if it succeeds, or $False, otherwise.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9169c-119">-ProductId</span><span class="sxs-lookup"><span data-stu-id="9169c-119">-ProductId</span></span>
<span data-ttu-id="9169c-120">指定要移除 API 的產品識別碼。</span><span class="sxs-lookup"><span data-stu-id="9169c-120">Specifies the ID of the product from which to remove the API.</span></span>

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

### <span data-ttu-id="9169c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9169c-121">CommonParameters</span></span>
<span data-ttu-id="9169c-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9169c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9169c-123">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9169c-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9169c-124">輸入</span><span class="sxs-lookup"><span data-stu-id="9169c-124">INPUTS</span></span>

### <span data-ttu-id="9169c-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="9169c-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9169c-126">System.String</span><span class="sxs-lookup"><span data-stu-id="9169c-126">System.String</span></span>

### <span data-ttu-id="9169c-127">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9169c-127">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9169c-128">輸出</span><span class="sxs-lookup"><span data-stu-id="9169c-128">OUTPUTS</span></span>

### <span data-ttu-id="9169c-129">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9169c-129">System.Boolean</span></span>

## <span data-ttu-id="9169c-130">筆記</span><span class="sxs-lookup"><span data-stu-id="9169c-130">NOTES</span></span>

## <span data-ttu-id="9169c-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="9169c-131">RELATED LINKS</span></span>

[<span data-ttu-id="9169c-132">Add-AzApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="9169c-132">Add-AzApiManagementApiToProduct</span></span>](./Add-AzApiManagementApiToProduct.md)


