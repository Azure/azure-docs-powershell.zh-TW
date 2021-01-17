---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 7C86B385-D784-45FD-9B57-31C895115A2C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementapitoproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToProduct.md
ms.openlocfilehash: 01767d80f0925647b2161dd26f504465d7f1d8e1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98447683"
---
# <span data-ttu-id="2d1cd-101">Add-AzApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="2d1cd-101">Add-AzApiManagementApiToProduct</span></span>

## <span data-ttu-id="2d1cd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2d1cd-102">SYNOPSIS</span></span>
<span data-ttu-id="2d1cd-103">在產品中加入 API。</span><span class="sxs-lookup"><span data-stu-id="2d1cd-103">Adds an API to a product.</span></span>

## <span data-ttu-id="2d1cd-104">句法</span><span class="sxs-lookup"><span data-stu-id="2d1cd-104">SYNTAX</span></span>

```
Add-AzApiManagementApiToProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d1cd-105">說明</span><span class="sxs-lookup"><span data-stu-id="2d1cd-105">DESCRIPTION</span></span>
<span data-ttu-id="2d1cd-106">**AzApiManagementApiToProduct** Cmdlet 會將 Azure API 管理 API 新增至產品。</span><span class="sxs-lookup"><span data-stu-id="2d1cd-106">The **Add-AzApiManagementApiToProduct** cmdlet adds an Azure API Management API to a product.</span></span>

## <span data-ttu-id="2d1cd-107">示例</span><span class="sxs-lookup"><span data-stu-id="2d1cd-107">EXAMPLES</span></span>

### <span data-ttu-id="2d1cd-108">範例1：新增 API 至產品</span><span class="sxs-lookup"><span data-stu-id="2d1cd-108">Example 1: Add an API to a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementApiToProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001"
```

<span data-ttu-id="2d1cd-109">這個命令會將指定的 API 新增至指定的產品。</span><span class="sxs-lookup"><span data-stu-id="2d1cd-109">This command adds the specified API to the specified product.</span></span>

## <span data-ttu-id="2d1cd-110">參數</span><span class="sxs-lookup"><span data-stu-id="2d1cd-110">PARAMETERS</span></span>

### <span data-ttu-id="2d1cd-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="2d1cd-111">-ApiId</span></span>
<span data-ttu-id="2d1cd-112">指定要新增至產品的 API 識別碼。</span><span class="sxs-lookup"><span data-stu-id="2d1cd-112">Specifies the ID of an API to add to a product.</span></span>

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

### <span data-ttu-id="2d1cd-113">-內容</span><span class="sxs-lookup"><span data-stu-id="2d1cd-113">-Context</span></span>
<span data-ttu-id="2d1cd-114">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="2d1cd-114">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d1cd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d1cd-115">-DefaultProfile</span></span>
<span data-ttu-id="2d1cd-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2d1cd-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d1cd-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2d1cd-117">-PassThru</span></span>
<span data-ttu-id="2d1cd-118">passthru</span><span class="sxs-lookup"><span data-stu-id="2d1cd-118">passthru</span></span>

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

### <span data-ttu-id="2d1cd-119">-產品識別碼</span><span class="sxs-lookup"><span data-stu-id="2d1cd-119">-ProductId</span></span>
<span data-ttu-id="2d1cd-120">指定要新增 API 的產品識別碼。</span><span class="sxs-lookup"><span data-stu-id="2d1cd-120">Specifies the ID of the product to which to add the API.</span></span>

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

### <span data-ttu-id="2d1cd-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d1cd-121">CommonParameters</span></span>
<span data-ttu-id="2d1cd-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2d1cd-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d1cd-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2d1cd-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d1cd-124">輸入</span><span class="sxs-lookup"><span data-stu-id="2d1cd-124">INPUTS</span></span>

### <span data-ttu-id="2d1cd-125">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="2d1cd-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2d1cd-126">System.object</span><span class="sxs-lookup"><span data-stu-id="2d1cd-126">System.String</span></span>

### <span data-ttu-id="2d1cd-127">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="2d1cd-127">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2d1cd-128">輸出</span><span class="sxs-lookup"><span data-stu-id="2d1cd-128">OUTPUTS</span></span>

### <span data-ttu-id="2d1cd-129">System.object</span><span class="sxs-lookup"><span data-stu-id="2d1cd-129">System.Boolean</span></span>

## <span data-ttu-id="2d1cd-130">筆記</span><span class="sxs-lookup"><span data-stu-id="2d1cd-130">NOTES</span></span>

## <span data-ttu-id="2d1cd-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="2d1cd-131">RELATED LINKS</span></span>

[<span data-ttu-id="2d1cd-132">移除-AzApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="2d1cd-132">Remove-AzApiManagementApiFromProduct</span></span>](./Remove-AzApiManagementApiFromProduct.md)


