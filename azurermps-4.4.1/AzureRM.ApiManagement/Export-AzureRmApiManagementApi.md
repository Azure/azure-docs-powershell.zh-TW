---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 2BA76B02-B786-4A77-86E0-E7D4191120B5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Export-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Export-AzureRmApiManagementApi.md
ms.openlocfilehash: 09400d3111ffb3fda232e1cbb71fd0aac063a74c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624860"
---
# <span data-ttu-id="0c5e5-101">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="0c5e5-101">Export-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="0c5e5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0c5e5-102">SYNOPSIS</span></span>
<span data-ttu-id="0c5e5-103">將 API 匯出至檔案。</span><span class="sxs-lookup"><span data-stu-id="0c5e5-103">Exports an API to a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c5e5-104">句法</span><span class="sxs-lookup"><span data-stu-id="0c5e5-104">SYNTAX</span></span>

### <span data-ttu-id="0c5e5-105">[匯出至管線] (預設) </span><span class="sxs-lookup"><span data-stu-id="0c5e5-105">Export to pipeline (Default)</span></span>
```
Export-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String>
 -SpecificationFormat <PsApiManagementApiFormat> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c5e5-106">匯出至檔案</span><span class="sxs-lookup"><span data-stu-id="0c5e5-106">Export to File</span></span>
```
Export-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String>
 -SpecificationFormat <PsApiManagementApiFormat> -SaveAs <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c5e5-107">說明</span><span class="sxs-lookup"><span data-stu-id="0c5e5-107">DESCRIPTION</span></span>
<span data-ttu-id="0c5e5-108">**Export AzureRmApiManagementApi** Cmdlet 會以其中一個支援的格式，將 Azure API 管理 API 匯出至檔案。</span><span class="sxs-lookup"><span data-stu-id="0c5e5-108">The **Export-AzureRmApiManagementApi** cmdlet exports an Azure API Management API to a file in one of the supported formats.</span></span>

## <span data-ttu-id="0c5e5-109">示例</span><span class="sxs-lookup"><span data-stu-id="0c5e5-109">EXAMPLES</span></span>

### <span data-ttu-id="0c5e5-110">範例1：在 Web 應用程式描述語言中匯出 API (WADL) 格式</span><span class="sxs-lookup"><span data-stu-id="0c5e5-110">Example 1: Export an API in Web Application Description Language (WADL) format</span></span>
```
PS C:\>Export-AzureRmApiManagementApi -Context $ApiMgmtContext -ApiId "0123456789" -SpecificationFormat "Wadl" -SaveAs "C:\contoso\specifications\0123456789.wadl"
```

<span data-ttu-id="0c5e5-111">這個命令會將 API 匯出至 WADL 檔案。</span><span class="sxs-lookup"><span data-stu-id="0c5e5-111">This command exports an API to a WADL file.</span></span>

## <span data-ttu-id="0c5e5-112">參數</span><span class="sxs-lookup"><span data-stu-id="0c5e5-112">PARAMETERS</span></span>

### <span data-ttu-id="0c5e5-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="0c5e5-113">-ApiId</span></span>
<span data-ttu-id="0c5e5-114">指定要匯出的 API 識別碼。</span><span class="sxs-lookup"><span data-stu-id="0c5e5-114">Specifies the ID of the API to export.</span></span>

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

### <span data-ttu-id="0c5e5-115">-內容</span><span class="sxs-lookup"><span data-stu-id="0c5e5-115">-Context</span></span>
<span data-ttu-id="0c5e5-116">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="0c5e5-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="0c5e5-117">-Force</span><span class="sxs-lookup"><span data-stu-id="0c5e5-117">-Force</span></span>
<span data-ttu-id="0c5e5-118">表示此操作會覆寫相同名稱的檔案（如果該檔案已存在）。</span><span class="sxs-lookup"><span data-stu-id="0c5e5-118">Indicates that this operation overwrites the file of the same name if it already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Export to File
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c5e5-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0c5e5-119">-PassThru</span></span>
<span data-ttu-id="0c5e5-120">表示此操作會在成功匯出 API 時傳回 $True，或 $False 其他方式。</span><span class="sxs-lookup"><span data-stu-id="0c5e5-120">Indicates that this operation returns $True if the API is exported successfully, or $False otherwise.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Export to File
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c5e5-121">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="0c5e5-121">-SaveAs</span></span>
<span data-ttu-id="0c5e5-122">指定要儲存匯出 API 的檔路徑。</span><span class="sxs-lookup"><span data-stu-id="0c5e5-122">Specifies the file path to which to save the exported API.</span></span>

```yaml
Type: System.String
Parameter Sets: Export to File
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c5e5-123">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="0c5e5-123">-SpecificationFormat</span></span>
<span data-ttu-id="0c5e5-124">指定 API 格式。</span><span class="sxs-lookup"><span data-stu-id="0c5e5-124">Specifies the API format.</span></span>
<span data-ttu-id="0c5e5-125">psdx_paramvalues Wadl 和 Swagger。</span><span class="sxs-lookup"><span data-stu-id="0c5e5-125">psdx_paramvalues Wadl and Swagger.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat
Parameter Sets: (All)
Aliases: 
Accepted values: Wadl, Swagger, Wsdl

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c5e5-126">-確認</span><span class="sxs-lookup"><span data-stu-id="0c5e5-126">-Confirm</span></span>
<span data-ttu-id="0c5e5-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0c5e5-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c5e5-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c5e5-128">-WhatIf</span></span>
<span data-ttu-id="0c5e5-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0c5e5-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c5e5-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0c5e5-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c5e5-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c5e5-131">-DefaultProfile</span></span>
<span data-ttu-id="0c5e5-132">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0c5e5-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c5e5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c5e5-133">CommonParameters</span></span>
<span data-ttu-id="0c5e5-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0c5e5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c5e5-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0c5e5-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c5e5-136">輸入</span><span class="sxs-lookup"><span data-stu-id="0c5e5-136">INPUTS</span></span>

## <span data-ttu-id="0c5e5-137">輸出</span><span class="sxs-lookup"><span data-stu-id="0c5e5-137">OUTPUTS</span></span>

### <span data-ttu-id="0c5e5-138">字串</span><span class="sxs-lookup"><span data-stu-id="0c5e5-138">String</span></span>
<span data-ttu-id="0c5e5-139">這個 Cmdlet 會以字串形式傳回匯出的 API 內容。</span><span class="sxs-lookup"><span data-stu-id="0c5e5-139">This cmdlet returns the exported API content as a string.</span></span>

## <span data-ttu-id="0c5e5-140">筆記</span><span class="sxs-lookup"><span data-stu-id="0c5e5-140">NOTES</span></span>

## <span data-ttu-id="0c5e5-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="0c5e5-141">RELATED LINKS</span></span>

[<span data-ttu-id="0c5e5-142">AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="0c5e5-142">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="0c5e5-143">匯入-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="0c5e5-143">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="0c5e5-144">新-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="0c5e5-144">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="0c5e5-145">移除-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="0c5e5-145">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="0c5e5-146">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="0c5e5-146">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


