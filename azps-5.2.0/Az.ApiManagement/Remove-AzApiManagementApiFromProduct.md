---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2457C7F5-7FB9-4712-AD7C-438E88F591A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapifromproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromProduct.md
ms.openlocfilehash: fd9e4cec821b08c9ac2bbd5cd2ac43e5e5b114ba
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281539"
---
# <span data-ttu-id="4848c-101">Remove-AzApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="4848c-101">Remove-AzApiManagementApiFromProduct</span></span>

## <span data-ttu-id="4848c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4848c-102">SYNOPSIS</span></span>
<span data-ttu-id="4848c-103">從產品移除 API。</span><span class="sxs-lookup"><span data-stu-id="4848c-103">Removes an API from a product.</span></span>

## <span data-ttu-id="4848c-104">句法</span><span class="sxs-lookup"><span data-stu-id="4848c-104">SYNTAX</span></span>

```
Remove-AzApiManagementApiFromProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4848c-105">說明</span><span class="sxs-lookup"><span data-stu-id="4848c-105">DESCRIPTION</span></span>
<span data-ttu-id="4848c-106">**AzApiManagementApiFromProduct** Cmdlet 會從產品中移除 Azure API 管理 API。</span><span class="sxs-lookup"><span data-stu-id="4848c-106">The **Remove-AzApiManagementApiFromProduct** cmdlet removes an Azure API Management API from a product.</span></span>

## <span data-ttu-id="4848c-107">示例</span><span class="sxs-lookup"><span data-stu-id="4848c-107">EXAMPLES</span></span>

### <span data-ttu-id="4848c-108">範例1：從產品移除 API</span><span class="sxs-lookup"><span data-stu-id="4848c-108">Example 1: Remove an API from a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiFromProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001" -PassThru
```

<span data-ttu-id="4848c-109">這個命令會從產品中移除指定的 API。</span><span class="sxs-lookup"><span data-stu-id="4848c-109">This command removes the specified API from a product.</span></span>

## <span data-ttu-id="4848c-110">參數</span><span class="sxs-lookup"><span data-stu-id="4848c-110">PARAMETERS</span></span>

### <span data-ttu-id="4848c-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="4848c-111">-ApiId</span></span>
<span data-ttu-id="4848c-112">指定要從產品中移除的 API 識別碼。</span><span class="sxs-lookup"><span data-stu-id="4848c-112">Specifies the ID of the API to remove from the product.</span></span>

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

### <span data-ttu-id="4848c-113">-內容</span><span class="sxs-lookup"><span data-stu-id="4848c-113">-Context</span></span>
<span data-ttu-id="4848c-114">指定 **PsApiManagementCoNtext**。</span><span class="sxs-lookup"><span data-stu-id="4848c-114">Specifies a **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="4848c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4848c-115">-DefaultProfile</span></span>
<span data-ttu-id="4848c-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4848c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4848c-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4848c-117">-PassThru</span></span>
<span data-ttu-id="4848c-118">指示這個 Cmdlet 會傳回 $True 的值（如果它成功的話），否則傳回 $False。</span><span class="sxs-lookup"><span data-stu-id="4848c-118">Indicates that this cmdlet returns a value of $True if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="4848c-119">-產品識別碼</span><span class="sxs-lookup"><span data-stu-id="4848c-119">-ProductId</span></span>
<span data-ttu-id="4848c-120">指定要從中移除 API 的產品識別碼。</span><span class="sxs-lookup"><span data-stu-id="4848c-120">Specifies the ID of the product from which to remove the API.</span></span>

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

### <span data-ttu-id="4848c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4848c-121">CommonParameters</span></span>
<span data-ttu-id="4848c-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4848c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4848c-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4848c-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4848c-124">輸入</span><span class="sxs-lookup"><span data-stu-id="4848c-124">INPUTS</span></span>

### <span data-ttu-id="4848c-125">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="4848c-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4848c-126">System.object</span><span class="sxs-lookup"><span data-stu-id="4848c-126">System.String</span></span>

### <span data-ttu-id="4848c-127">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="4848c-127">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4848c-128">輸出</span><span class="sxs-lookup"><span data-stu-id="4848c-128">OUTPUTS</span></span>

### <span data-ttu-id="4848c-129">System.object</span><span class="sxs-lookup"><span data-stu-id="4848c-129">System.Boolean</span></span>

## <span data-ttu-id="4848c-130">筆記</span><span class="sxs-lookup"><span data-stu-id="4848c-130">NOTES</span></span>

## <span data-ttu-id="4848c-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="4848c-131">RELATED LINKS</span></span>

[<span data-ttu-id="4848c-132">附加 AzApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="4848c-132">Add-AzApiManagementApiToProduct</span></span>](./Add-AzApiManagementApiToProduct.md)


