---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2457C7F5-7FB9-4712-AD7C-438E88F591A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapifromproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromProduct.md
ms.openlocfilehash: fd9e4cec821b08c9ac2bbd5cd2ac43e5e5b114ba
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129692"
---
# <span data-ttu-id="45f3e-101">Remove-AzApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="45f3e-101">Remove-AzApiManagementApiFromProduct</span></span>

## <span data-ttu-id="45f3e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="45f3e-102">SYNOPSIS</span></span>
<span data-ttu-id="45f3e-103">從產品移除 API。</span><span class="sxs-lookup"><span data-stu-id="45f3e-103">Removes an API from a product.</span></span>

## <span data-ttu-id="45f3e-104">句法</span><span class="sxs-lookup"><span data-stu-id="45f3e-104">SYNTAX</span></span>

```
Remove-AzApiManagementApiFromProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45f3e-105">說明</span><span class="sxs-lookup"><span data-stu-id="45f3e-105">DESCRIPTION</span></span>
<span data-ttu-id="45f3e-106">**AzApiManagementApiFromProduct** Cmdlet 會從產品中移除 Azure API 管理 API。</span><span class="sxs-lookup"><span data-stu-id="45f3e-106">The **Remove-AzApiManagementApiFromProduct** cmdlet removes an Azure API Management API from a product.</span></span>

## <span data-ttu-id="45f3e-107">示例</span><span class="sxs-lookup"><span data-stu-id="45f3e-107">EXAMPLES</span></span>

### <span data-ttu-id="45f3e-108">範例1：從產品移除 API</span><span class="sxs-lookup"><span data-stu-id="45f3e-108">Example 1: Remove an API from a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiFromProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001" -PassThru
```

<span data-ttu-id="45f3e-109">這個命令會從產品中移除指定的 API。</span><span class="sxs-lookup"><span data-stu-id="45f3e-109">This command removes the specified API from a product.</span></span>

## <span data-ttu-id="45f3e-110">參數</span><span class="sxs-lookup"><span data-stu-id="45f3e-110">PARAMETERS</span></span>

### <span data-ttu-id="45f3e-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="45f3e-111">-ApiId</span></span>
<span data-ttu-id="45f3e-112">指定要從產品中移除的 API 識別碼。</span><span class="sxs-lookup"><span data-stu-id="45f3e-112">Specifies the ID of the API to remove from the product.</span></span>

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

### <span data-ttu-id="45f3e-113">-內容</span><span class="sxs-lookup"><span data-stu-id="45f3e-113">-Context</span></span>
<span data-ttu-id="45f3e-114">指定 **PsApiManagementCoNtext** 。</span><span class="sxs-lookup"><span data-stu-id="45f3e-114">Specifies a **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="45f3e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45f3e-115">-DefaultProfile</span></span>
<span data-ttu-id="45f3e-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="45f3e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45f3e-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="45f3e-117">-PassThru</span></span>
<span data-ttu-id="45f3e-118">指示這個 Cmdlet 會傳回 $True 的值（如果它成功的話），否則傳回 $False。</span><span class="sxs-lookup"><span data-stu-id="45f3e-118">Indicates that this cmdlet returns a value of $True if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="45f3e-119">-產品識別碼</span><span class="sxs-lookup"><span data-stu-id="45f3e-119">-ProductId</span></span>
<span data-ttu-id="45f3e-120">指定要從中移除 API 的產品識別碼。</span><span class="sxs-lookup"><span data-stu-id="45f3e-120">Specifies the ID of the product from which to remove the API.</span></span>

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

### <span data-ttu-id="45f3e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45f3e-121">CommonParameters</span></span>
<span data-ttu-id="45f3e-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="45f3e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45f3e-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="45f3e-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45f3e-124">輸入</span><span class="sxs-lookup"><span data-stu-id="45f3e-124">INPUTS</span></span>

### <span data-ttu-id="45f3e-125">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="45f3e-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="45f3e-126">System.object</span><span class="sxs-lookup"><span data-stu-id="45f3e-126">System.String</span></span>

### <span data-ttu-id="45f3e-127">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="45f3e-127">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="45f3e-128">輸出</span><span class="sxs-lookup"><span data-stu-id="45f3e-128">OUTPUTS</span></span>

### <span data-ttu-id="45f3e-129">System.object</span><span class="sxs-lookup"><span data-stu-id="45f3e-129">System.Boolean</span></span>

## <span data-ttu-id="45f3e-130">筆記</span><span class="sxs-lookup"><span data-stu-id="45f3e-130">NOTES</span></span>

## <span data-ttu-id="45f3e-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="45f3e-131">RELATED LINKS</span></span>

[<span data-ttu-id="45f3e-132">附加 AzApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="45f3e-132">Add-AzApiManagementApiToProduct</span></span>](./Add-AzApiManagementApiToProduct.md)


