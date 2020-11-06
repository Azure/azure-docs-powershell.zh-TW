---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2457C7F5-7FB9-4712-AD7C-438E88F591A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapifromproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromProduct.md
ms.openlocfilehash: 497e830ff5ee51a9b18480a4d3f31f7c51949723
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613947"
---
# <span data-ttu-id="37204-101">Remove-AzApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="37204-101">Remove-AzApiManagementApiFromProduct</span></span>

## <span data-ttu-id="37204-102">摘要</span><span class="sxs-lookup"><span data-stu-id="37204-102">SYNOPSIS</span></span>
<span data-ttu-id="37204-103">從產品移除 API。</span><span class="sxs-lookup"><span data-stu-id="37204-103">Removes an API from a product.</span></span>

## <span data-ttu-id="37204-104">句法</span><span class="sxs-lookup"><span data-stu-id="37204-104">SYNTAX</span></span>

```
Remove-AzApiManagementApiFromProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37204-105">說明</span><span class="sxs-lookup"><span data-stu-id="37204-105">DESCRIPTION</span></span>
<span data-ttu-id="37204-106">**AzApiManagementApiFromProduct** Cmdlet 會從產品中移除 Azure API 管理 API。</span><span class="sxs-lookup"><span data-stu-id="37204-106">The **Remove-AzApiManagementApiFromProduct** cmdlet removes an Azure API Management API from a product.</span></span>

## <span data-ttu-id="37204-107">示例</span><span class="sxs-lookup"><span data-stu-id="37204-107">EXAMPLES</span></span>

### <span data-ttu-id="37204-108">範例1：從產品移除 API</span><span class="sxs-lookup"><span data-stu-id="37204-108">Example 1: Remove an API from a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiFromProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001" -PassThru
```

<span data-ttu-id="37204-109">這個命令會從產品中移除指定的 API。</span><span class="sxs-lookup"><span data-stu-id="37204-109">This command removes the specified API from a product.</span></span>

## <span data-ttu-id="37204-110">參數</span><span class="sxs-lookup"><span data-stu-id="37204-110">PARAMETERS</span></span>

### <span data-ttu-id="37204-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="37204-111">-ApiId</span></span>
<span data-ttu-id="37204-112">指定要從產品中移除的 API 識別碼。</span><span class="sxs-lookup"><span data-stu-id="37204-112">Specifies the ID of the API to remove from the product.</span></span>

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

### <span data-ttu-id="37204-113">-內容</span><span class="sxs-lookup"><span data-stu-id="37204-113">-Context</span></span>
<span data-ttu-id="37204-114">指定 **PsApiManagementCoNtext** 。</span><span class="sxs-lookup"><span data-stu-id="37204-114">Specifies a **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="37204-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37204-115">-DefaultProfile</span></span>
<span data-ttu-id="37204-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="37204-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37204-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="37204-117">-PassThru</span></span>
<span data-ttu-id="37204-118">指示這個 Cmdlet 會傳回 $True 的值（如果它成功的話），否則傳回 $False。</span><span class="sxs-lookup"><span data-stu-id="37204-118">Indicates that this cmdlet returns a value of $True if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="37204-119">-產品識別碼</span><span class="sxs-lookup"><span data-stu-id="37204-119">-ProductId</span></span>
<span data-ttu-id="37204-120">指定要從中移除 API 的產品識別碼。</span><span class="sxs-lookup"><span data-stu-id="37204-120">Specifies the ID of the product from which to remove the API.</span></span>

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

### <span data-ttu-id="37204-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37204-121">CommonParameters</span></span>
<span data-ttu-id="37204-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="37204-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37204-123">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="37204-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37204-124">輸入</span><span class="sxs-lookup"><span data-stu-id="37204-124">INPUTS</span></span>

### <span data-ttu-id="37204-125">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="37204-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="37204-126">System.object</span><span class="sxs-lookup"><span data-stu-id="37204-126">System.String</span></span>

### <span data-ttu-id="37204-127">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="37204-127">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="37204-128">輸出</span><span class="sxs-lookup"><span data-stu-id="37204-128">OUTPUTS</span></span>

### <span data-ttu-id="37204-129">System.object</span><span class="sxs-lookup"><span data-stu-id="37204-129">System.Boolean</span></span>

## <span data-ttu-id="37204-130">筆記</span><span class="sxs-lookup"><span data-stu-id="37204-130">NOTES</span></span>

## <span data-ttu-id="37204-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="37204-131">RELATED LINKS</span></span>

[<span data-ttu-id="37204-132">附加 AzApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="37204-132">Add-AzApiManagementApiToProduct</span></span>](./Add-AzApiManagementApiToProduct.md)


