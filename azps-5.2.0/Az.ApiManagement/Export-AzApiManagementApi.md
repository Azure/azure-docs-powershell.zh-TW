---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2BA76B02-B786-4A77-86E0-E7D4191120B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/export-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Export-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Export-AzApiManagementApi.md
ms.openlocfilehash: 3981d1fd0a921f467007afc85c00b726b6037fad
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98280359"
---
# <span data-ttu-id="e8240-101">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e8240-101">Export-AzApiManagementApi</span></span>

## <span data-ttu-id="e8240-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e8240-102">SYNOPSIS</span></span>
<span data-ttu-id="e8240-103">將 API 匯出至檔案。</span><span class="sxs-lookup"><span data-stu-id="e8240-103">Exports an API to a file.</span></span>

## <span data-ttu-id="e8240-104">句法</span><span class="sxs-lookup"><span data-stu-id="e8240-104">SYNTAX</span></span>

### <span data-ttu-id="e8240-105">ExportToPipeline (預設) </span><span class="sxs-lookup"><span data-stu-id="e8240-105">ExportToPipeline (Default)</span></span>
```
Export-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8240-106">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="e8240-106">ExportToFile</span></span>
```
Export-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SaveAs <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8240-107">說明</span><span class="sxs-lookup"><span data-stu-id="e8240-107">DESCRIPTION</span></span>
<span data-ttu-id="e8240-108">**Export AzApiManagementApi** Cmdlet 會以其中一個支援的格式，將 Azure API 管理 API 匯出至檔案。</span><span class="sxs-lookup"><span data-stu-id="e8240-108">The **Export-AzApiManagementApi** cmdlet exports an Azure API Management API to a file in one of the supported formats.</span></span>

## <span data-ttu-id="e8240-109">示例</span><span class="sxs-lookup"><span data-stu-id="e8240-109">EXAMPLES</span></span>

### <span data-ttu-id="e8240-110">範例1：在 Web 應用程式描述語言中匯出 API (WADL) 格式</span><span class="sxs-lookup"><span data-stu-id="e8240-110">Example 1: Export an API in Web Application Description Language (WADL) format</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Export-AzApiManagementApi -Context $ApiMgmtContext -ApiId "0123456789" -SpecificationFormat "Wadl" -SaveAs "C:\contoso\specifications\0123456789.wadl"
```

<span data-ttu-id="e8240-111">這個命令會將 API 匯出至 WADL 檔案。</span><span class="sxs-lookup"><span data-stu-id="e8240-111">This command exports an API to a WADL file.</span></span>

### <span data-ttu-id="e8240-112">範例2：將 OpenApi 3.0 規格格式的 API 匯出為 Json 檔</span><span class="sxs-lookup"><span data-stu-id="e8240-112">Example 2: Export an API in OpenApi 3.0 Specification Format as Json Document</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Export-AzApiManagementApi -Context $context -ApiId swagger-petstore -SpecificationFormat OpenApiJson -SaveAs D:\github\petstore.json
```

<span data-ttu-id="e8240-113">這個命令會將 Open Api 格式的 API 定義匯出為 Json 檔</span><span class="sxs-lookup"><span data-stu-id="e8240-113">This command exports an API definitions in Open Api format as Json document</span></span>

## <span data-ttu-id="e8240-114">參數</span><span class="sxs-lookup"><span data-stu-id="e8240-114">PARAMETERS</span></span>

### <span data-ttu-id="e8240-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="e8240-115">-ApiId</span></span>
<span data-ttu-id="e8240-116">指定要匯出的 API 識別碼。</span><span class="sxs-lookup"><span data-stu-id="e8240-116">Specifies the ID of the API to export.</span></span>

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

### <span data-ttu-id="e8240-117">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="e8240-117">-ApiRevision</span></span>
<span data-ttu-id="e8240-118">API 修訂的識別碼。</span><span class="sxs-lookup"><span data-stu-id="e8240-118">Identifier of API Revision.</span></span> <span data-ttu-id="e8240-119">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="e8240-119">This parameter is optional.</span></span> <span data-ttu-id="e8240-120">如果沒有指定，則會針對目前使用中的 api 修正進行匯出。</span><span class="sxs-lookup"><span data-stu-id="e8240-120">If not specified, the export will be done for the currently active api revision.</span></span>

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

### <span data-ttu-id="e8240-121">-內容</span><span class="sxs-lookup"><span data-stu-id="e8240-121">-Context</span></span>
<span data-ttu-id="e8240-122">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="e8240-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="e8240-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8240-123">-DefaultProfile</span></span>
<span data-ttu-id="e8240-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e8240-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8240-125">-Force</span><span class="sxs-lookup"><span data-stu-id="e8240-125">-Force</span></span>
<span data-ttu-id="e8240-126">表示此操作會覆寫相同名稱的檔案（如果該檔案已存在）。</span><span class="sxs-lookup"><span data-stu-id="e8240-126">Indicates that this operation overwrites the file of the same name if it already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExportToFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8240-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e8240-127">-PassThru</span></span>
<span data-ttu-id="e8240-128">表示此操作會在成功匯出 API 時傳回 $True，或 $False 其他方式。</span><span class="sxs-lookup"><span data-stu-id="e8240-128">Indicates that this operation returns $True if the API is exported successfully, or $False otherwise.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExportToFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8240-129">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="e8240-129">-SaveAs</span></span>
<span data-ttu-id="e8240-130">指定要儲存匯出 API 的檔路徑。</span><span class="sxs-lookup"><span data-stu-id="e8240-130">Specifies the file path to which to save the exported API.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportToFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8240-131">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="e8240-131">-SpecificationFormat</span></span>
<span data-ttu-id="e8240-132">指定 API 格式。</span><span class="sxs-lookup"><span data-stu-id="e8240-132">Specifies the API format.</span></span>
<span data-ttu-id="e8240-133">psdx_paramvalues Wadl、Wsdl、Swagger、OpenApi 和 OpenApiJson</span><span class="sxs-lookup"><span data-stu-id="e8240-133">psdx_paramvalues Wadl, Wsdl, Swagger, OpenApi and OpenApiJson</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat
Parameter Sets: (All)
Aliases:
Accepted values: Wadl, Swagger, Wsdl, OpenApi, OpenApiJson

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8240-134">-確認</span><span class="sxs-lookup"><span data-stu-id="e8240-134">-Confirm</span></span>
<span data-ttu-id="e8240-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e8240-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8240-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8240-136">-WhatIf</span></span>
<span data-ttu-id="e8240-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e8240-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8240-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e8240-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8240-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8240-139">CommonParameters</span></span>
<span data-ttu-id="e8240-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e8240-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8240-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e8240-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8240-142">輸入</span><span class="sxs-lookup"><span data-stu-id="e8240-142">INPUTS</span></span>

### <span data-ttu-id="e8240-143">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="e8240-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e8240-144">System.object</span><span class="sxs-lookup"><span data-stu-id="e8240-144">System.String</span></span>

### <span data-ttu-id="e8240-145">ServiceManagement. PsApiManagementApiFormat （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="e8240-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span></span>

### <span data-ttu-id="e8240-146">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="e8240-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e8240-147">輸出</span><span class="sxs-lookup"><span data-stu-id="e8240-147">OUTPUTS</span></span>

### <span data-ttu-id="e8240-148">System.object</span><span class="sxs-lookup"><span data-stu-id="e8240-148">System.String</span></span>

## <span data-ttu-id="e8240-149">筆記</span><span class="sxs-lookup"><span data-stu-id="e8240-149">NOTES</span></span>

## <span data-ttu-id="e8240-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="e8240-150">RELATED LINKS</span></span>

[<span data-ttu-id="e8240-151">AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e8240-151">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="e8240-152">匯入-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e8240-152">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="e8240-153">新-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e8240-153">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="e8240-154">移除-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e8240-154">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="e8240-155">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e8240-155">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


