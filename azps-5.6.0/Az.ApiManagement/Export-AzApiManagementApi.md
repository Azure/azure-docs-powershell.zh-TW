---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2BA76B02-B786-4A77-86E0-E7D4191120B5
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/export-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Export-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Export-AzApiManagementApi.md
ms.openlocfilehash: 9f65550f9a3e1aec9e0f44fa2e436f715e23f948
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910329"
---
# <span data-ttu-id="5cd27-101">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="5cd27-101">Export-AzApiManagementApi</span></span>

## <span data-ttu-id="5cd27-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5cd27-102">SYNOPSIS</span></span>
<span data-ttu-id="5cd27-103">將 API 匯出至檔案。</span><span class="sxs-lookup"><span data-stu-id="5cd27-103">Exports an API to a file.</span></span>

## <span data-ttu-id="5cd27-104">語法</span><span class="sxs-lookup"><span data-stu-id="5cd27-104">SYNTAX</span></span>

### <span data-ttu-id="5cd27-105">ExportToPipeline (預設) </span><span class="sxs-lookup"><span data-stu-id="5cd27-105">ExportToPipeline (Default)</span></span>
```
Export-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cd27-106">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="5cd27-106">ExportToFile</span></span>
```
Export-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SaveAs <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5cd27-107">描述</span><span class="sxs-lookup"><span data-stu-id="5cd27-107">DESCRIPTION</span></span>
<span data-ttu-id="5cd27-108">**Export-AzApiManagementApi** Cmdlet 會匯出 Azure API 管理 API 至其中一種支援格式的檔案。</span><span class="sxs-lookup"><span data-stu-id="5cd27-108">The **Export-AzApiManagementApi** cmdlet exports an Azure API Management API to a file in one of the supported formats.</span></span>

## <span data-ttu-id="5cd27-109">例子</span><span class="sxs-lookup"><span data-stu-id="5cd27-109">EXAMPLES</span></span>

### <span data-ttu-id="5cd27-110">範例 1：將 API 匯出為 Web 應用程式描述語言 (WADL) 格式</span><span class="sxs-lookup"><span data-stu-id="5cd27-110">Example 1: Export an API in Web Application Description Language (WADL) format</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Export-AzApiManagementApi -Context $ApiMgmtContext -ApiId "0123456789" -SpecificationFormat "Wadl" -SaveAs "C:\contoso\specifications\0123456789.wadl"
```

<span data-ttu-id="5cd27-111">此命令會匯出 API 至 WADL 檔案。</span><span class="sxs-lookup"><span data-stu-id="5cd27-111">This command exports an API to a WADL file.</span></span>

### <span data-ttu-id="5cd27-112">範例 2：將 OpenApi 3.0 規格格式的 API 匯出為 Json 檔</span><span class="sxs-lookup"><span data-stu-id="5cd27-112">Example 2: Export an API in OpenApi 3.0 Specification Format as Json Document</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Export-AzApiManagementApi -Context $context -ApiId swagger-petstore -SpecificationFormat OpenApiJson -SaveAs D:\github\petstore.json
```

<span data-ttu-id="5cd27-113">此命令會以 Open Api 格式將 API 定義匯出為 Json 檔</span><span class="sxs-lookup"><span data-stu-id="5cd27-113">This command exports an API definitions in Open Api format as Json document</span></span>

## <span data-ttu-id="5cd27-114">參數</span><span class="sxs-lookup"><span data-stu-id="5cd27-114">PARAMETERS</span></span>

### <span data-ttu-id="5cd27-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="5cd27-115">-ApiId</span></span>
<span data-ttu-id="5cd27-116">指定要匯出的 API 識別碼。</span><span class="sxs-lookup"><span data-stu-id="5cd27-116">Specifies the ID of the API to export.</span></span>

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

### <span data-ttu-id="5cd27-117">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="5cd27-117">-ApiRevision</span></span>
<span data-ttu-id="5cd27-118">API 修訂的識別碼。</span><span class="sxs-lookup"><span data-stu-id="5cd27-118">Identifier of API Revision.</span></span> <span data-ttu-id="5cd27-119">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="5cd27-119">This parameter is optional.</span></span> <span data-ttu-id="5cd27-120">如果未指定，將會針對目前使用中的 Api 修訂完成匯出。</span><span class="sxs-lookup"><span data-stu-id="5cd27-120">If not specified, the export will be done for the currently active api revision.</span></span>

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

### <span data-ttu-id="5cd27-121">-內容</span><span class="sxs-lookup"><span data-stu-id="5cd27-121">-Context</span></span>
<span data-ttu-id="5cd27-122">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="5cd27-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="5cd27-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cd27-123">-DefaultProfile</span></span>
<span data-ttu-id="5cd27-124">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5cd27-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5cd27-125">-強制</span><span class="sxs-lookup"><span data-stu-id="5cd27-125">-Force</span></span>
<span data-ttu-id="5cd27-126">表示此作業會覆寫已存在相同名稱的檔案。</span><span class="sxs-lookup"><span data-stu-id="5cd27-126">Indicates that this operation overwrites the file of the same name if it already exists.</span></span>

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

### <span data-ttu-id="5cd27-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5cd27-127">-PassThru</span></span>
<span data-ttu-id="5cd27-128">表示此作業會$True成功匯出 API，否則會$False匯出。</span><span class="sxs-lookup"><span data-stu-id="5cd27-128">Indicates that this operation returns $True if the API is exported successfully, or $False otherwise.</span></span>

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

### <span data-ttu-id="5cd27-129">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="5cd27-129">-SaveAs</span></span>
<span data-ttu-id="5cd27-130">指定儲存匯出 API 的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="5cd27-130">Specifies the file path to which to save the exported API.</span></span>

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

### <span data-ttu-id="5cd27-131">-規格格式</span><span class="sxs-lookup"><span data-stu-id="5cd27-131">-SpecificationFormat</span></span>
<span data-ttu-id="5cd27-132">指定 API 格式。</span><span class="sxs-lookup"><span data-stu-id="5cd27-132">Specifies the API format.</span></span>
<span data-ttu-id="5cd27-133">psdx_paramvalues Wadl、Wsdl、Swagger、OpenApi 和 OpenApiJson</span><span class="sxs-lookup"><span data-stu-id="5cd27-133">psdx_paramvalues Wadl, Wsdl, Swagger, OpenApi and OpenApiJson</span></span>

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

### <span data-ttu-id="5cd27-134">-確認</span><span class="sxs-lookup"><span data-stu-id="5cd27-134">-Confirm</span></span>
<span data-ttu-id="5cd27-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="5cd27-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cd27-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cd27-136">-WhatIf</span></span>
<span data-ttu-id="5cd27-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5cd27-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5cd27-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5cd27-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cd27-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cd27-139">CommonParameters</span></span>
<span data-ttu-id="5cd27-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5cd27-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cd27-141">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5cd27-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cd27-142">輸入</span><span class="sxs-lookup"><span data-stu-id="5cd27-142">INPUTS</span></span>

### <span data-ttu-id="5cd27-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="5cd27-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5cd27-144">System.String</span><span class="sxs-lookup"><span data-stu-id="5cd27-144">System.String</span></span>

### <span data-ttu-id="5cd27-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementApiFormat</span><span class="sxs-lookup"><span data-stu-id="5cd27-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span></span>

### <span data-ttu-id="5cd27-146">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5cd27-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5cd27-147">輸出</span><span class="sxs-lookup"><span data-stu-id="5cd27-147">OUTPUTS</span></span>

### <span data-ttu-id="5cd27-148">System.String</span><span class="sxs-lookup"><span data-stu-id="5cd27-148">System.String</span></span>

## <span data-ttu-id="5cd27-149">筆記</span><span class="sxs-lookup"><span data-stu-id="5cd27-149">NOTES</span></span>

## <span data-ttu-id="5cd27-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="5cd27-150">RELATED LINKS</span></span>

[<span data-ttu-id="5cd27-151">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="5cd27-151">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="5cd27-152">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="5cd27-152">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="5cd27-153">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="5cd27-153">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="5cd27-154">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="5cd27-154">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="5cd27-155">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="5cd27-155">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


