---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 7BCEB0EF-1A09-4CED-9F34-CE3AB03181A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementPolicy.md
ms.openlocfilehash: dc0d985203d51c705c40b423d0b6c9f381fa87e4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957867"
---
# <span data-ttu-id="fabeb-101">Get-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="fabeb-101">Get-AzApiManagementPolicy</span></span>

## <span data-ttu-id="fabeb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fabeb-102">SYNOPSIS</span></span>
<span data-ttu-id="fabeb-103">取得指定的範圍原則。</span><span class="sxs-lookup"><span data-stu-id="fabeb-103">Gets the specified scope policy.</span></span>

## <span data-ttu-id="fabeb-104">句法</span><span class="sxs-lookup"><span data-stu-id="fabeb-104">SYNTAX</span></span>

### <span data-ttu-id="fabeb-105">GetTenantLevel (預設) </span><span class="sxs-lookup"><span data-stu-id="fabeb-105">GetTenantLevel (Default)</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fabeb-106">GetProductLevel</span><span class="sxs-lookup"><span data-stu-id="fabeb-106">GetProductLevel</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ProductId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fabeb-107">GetApiLevel</span><span class="sxs-lookup"><span data-stu-id="fabeb-107">GetApiLevel</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-ApiRevision <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fabeb-108">GetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="fabeb-108">GetOperationLevel</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-ApiRevision <String>] -OperationId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fabeb-109">說明</span><span class="sxs-lookup"><span data-stu-id="fabeb-109">DESCRIPTION</span></span>
<span data-ttu-id="fabeb-110">**AzApiManagementPolicy** Cmdlet 會取得指定的範圍原則。</span><span class="sxs-lookup"><span data-stu-id="fabeb-110">The **Get-AzApiManagementPolicy** cmdlet gets the specified scope policy.</span></span>

## <span data-ttu-id="fabeb-111">示例</span><span class="sxs-lookup"><span data-stu-id="fabeb-111">EXAMPLES</span></span>

### <span data-ttu-id="fabeb-112">範例1：取得租使用者層級原則</span><span class="sxs-lookup"><span data-stu-id="fabeb-112">Example 1: Get the tenant level policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -SaveAs "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="fabeb-113">這個命令會取得租使用者層級原則，並將它儲存到名為 tenantpolicy.xml 的檔案。</span><span class="sxs-lookup"><span data-stu-id="fabeb-113">This command gets tenant level policy and saves it to a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="fabeb-114">範例2：取得產品範圍原則</span><span class="sxs-lookup"><span data-stu-id="fabeb-114">Example 2: Get the product-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="fabeb-115">這個命令會取得產品範圍原則</span><span class="sxs-lookup"><span data-stu-id="fabeb-115">This command gets product-scope policy</span></span>

### <span data-ttu-id="fabeb-116">範例3：取得 API 範圍原則</span><span class="sxs-lookup"><span data-stu-id="fabeb-116">Example 3: Get the API-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

<span data-ttu-id="fabeb-117">這個命令會取得 API 作用域原則。</span><span class="sxs-lookup"><span data-stu-id="fabeb-117">This command gets API-scope policy.</span></span>

### <span data-ttu-id="fabeb-118">範例4：取得操作範圍原則</span><span class="sxs-lookup"><span data-stu-id="fabeb-118">Example 4: Get the operation-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="fabeb-119">這個命令會取得操作範圍原則。</span><span class="sxs-lookup"><span data-stu-id="fabeb-119">This command gets the operation-scope policy.</span></span>

### <span data-ttu-id="fabeb-120">範例5：以 RawXml 格式取得租使用者範圍原則</span><span class="sxs-lookup"><span data-stu-id="fabeb-120">Example 5: Get the Tenant scope policy in RawXml format</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS c:\> Get-AzApiManagementPolicy -Context $context -Format rawxml

<policies>
        <inbound>
                <set-header name="correlationid" exists-action="skip">
                        <value>@{
                var guidBinary = new byte[16];
                Array.Copy(Guid.NewGuid().ToByteArray(), 0, guidBinary, 0, 10);
                long time = DateTime.Now.Ticks;
                byte[] bytes = new byte[6];
                unchecked
                {
                       bytes[5] = (byte)(time >> 40);
                       bytes[4] = (byte)(time >> 32);
                       bytes[3] = (byte)(time >> 24);
                       bytes[2] = (byte)(time >> 16);
                       bytes[1] = (byte)(time >> 8);
                       bytes[0] = (byte)(time);
                }
                Array.Copy(bytes, 0, guidBinary, 10, 6);
                return new Guid(guidBinary).ToString();
            }
            </value>
                </set-header>
        </inbound>
        <backend>
                <forward-request />
        </backend>
        <outbound />
        <on-error />
</policies>
```

<span data-ttu-id="fabeb-121">這個命令會以非 Xml 轉義格式取得租使用者範圍原則。</span><span class="sxs-lookup"><span data-stu-id="fabeb-121">This command gets the tenant-scope policy in Non-Xml escaped format.</span></span>

## <span data-ttu-id="fabeb-122">參數</span><span class="sxs-lookup"><span data-stu-id="fabeb-122">PARAMETERS</span></span>

### <span data-ttu-id="fabeb-123">-ApiId</span><span class="sxs-lookup"><span data-stu-id="fabeb-123">-ApiId</span></span>
<span data-ttu-id="fabeb-124">指定現有 API 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="fabeb-124">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="fabeb-125">如果您指定此參數，則 Cmdlet 會傳回 API 範圍原則。</span><span class="sxs-lookup"><span data-stu-id="fabeb-125">If you specify this parameter the cmdlet returns the API-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetApiLevel, GetOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fabeb-126">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="fabeb-126">-ApiRevision</span></span>
<span data-ttu-id="fabeb-127">API 修訂的識別碼。</span><span class="sxs-lookup"><span data-stu-id="fabeb-127">Identifier of API Revision.</span></span> <span data-ttu-id="fabeb-128">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="fabeb-128">This parameter is optional.</span></span> <span data-ttu-id="fabeb-129">如果未指定，將會從目前使用中的 api 修訂中檢索原則。</span><span class="sxs-lookup"><span data-stu-id="fabeb-129">If not specified, the policy will be retrieved from the currently active api revision.</span></span>

```yaml
Type: System.String
Parameter Sets: GetApiLevel, GetOperationLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fabeb-130">-內容</span><span class="sxs-lookup"><span data-stu-id="fabeb-130">-Context</span></span>
<span data-ttu-id="fabeb-131">指定 **PsApiManagementCoNtext** 的實例。</span><span class="sxs-lookup"><span data-stu-id="fabeb-131">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="fabeb-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fabeb-132">-DefaultProfile</span></span>
<span data-ttu-id="fabeb-133">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fabeb-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fabeb-134">-Force</span><span class="sxs-lookup"><span data-stu-id="fabeb-134">-Force</span></span>
<span data-ttu-id="fabeb-135">ps_force</span><span class="sxs-lookup"><span data-stu-id="fabeb-135">ps_force</span></span>

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

### <span data-ttu-id="fabeb-136">-Format</span><span class="sxs-lookup"><span data-stu-id="fabeb-136">-Format</span></span>
<span data-ttu-id="fabeb-137">指定 API 管理原則的格式。</span><span class="sxs-lookup"><span data-stu-id="fabeb-137">Specifies the format of the API management policy.</span></span>
<span data-ttu-id="fabeb-138">此參數的預設值為 "xml"。</span><span class="sxs-lookup"><span data-stu-id="fabeb-138">The default value for this parameter is "xml".</span></span>

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

### <span data-ttu-id="fabeb-139">-OperationId</span><span class="sxs-lookup"><span data-stu-id="fabeb-139">-OperationId</span></span>
<span data-ttu-id="fabeb-140">指定現有 API 操作的識別碼。</span><span class="sxs-lookup"><span data-stu-id="fabeb-140">Specifies the identifier of the existing API operation.</span></span>
<span data-ttu-id="fabeb-141">如果您使用 *ApiId* 指定此參數，則 Cmdlet 會傳回 operation 範圍原則。</span><span class="sxs-lookup"><span data-stu-id="fabeb-141">If you specify this parameter with *ApiId* the cmdlet returns operation-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fabeb-142">-產品識別碼</span><span class="sxs-lookup"><span data-stu-id="fabeb-142">-ProductId</span></span>
<span data-ttu-id="fabeb-143">指定現有產品的識別碼。</span><span class="sxs-lookup"><span data-stu-id="fabeb-143">Specifies the identifier of an existing product.</span></span>
<span data-ttu-id="fabeb-144">如果您指定此參數，則 Cmdlet 會傳回產品範圍原則。</span><span class="sxs-lookup"><span data-stu-id="fabeb-144">If you specify this parameter the cmdlet returns the product-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetProductLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fabeb-145">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="fabeb-145">-SaveAs</span></span>
<span data-ttu-id="fabeb-146">指定要儲存結果的檔路徑。</span><span class="sxs-lookup"><span data-stu-id="fabeb-146">Specifies the file path to save the result to.</span></span>
<span data-ttu-id="fabeb-147">如果您沒有指定此參數，結果就會以流水線為 sting。</span><span class="sxs-lookup"><span data-stu-id="fabeb-147">If you do not specify this parameter the result is pipelined as a sting.</span></span>

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

### <span data-ttu-id="fabeb-148">-確認</span><span class="sxs-lookup"><span data-stu-id="fabeb-148">-Confirm</span></span>
<span data-ttu-id="fabeb-149">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fabeb-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fabeb-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fabeb-150">-WhatIf</span></span>
<span data-ttu-id="fabeb-151">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fabeb-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fabeb-152">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fabeb-152">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fabeb-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fabeb-153">CommonParameters</span></span>
<span data-ttu-id="fabeb-154">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fabeb-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fabeb-155">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="fabeb-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fabeb-156">輸入</span><span class="sxs-lookup"><span data-stu-id="fabeb-156">INPUTS</span></span>

### <span data-ttu-id="fabeb-157">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="fabeb-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="fabeb-158">System.object</span><span class="sxs-lookup"><span data-stu-id="fabeb-158">System.String</span></span>

### <span data-ttu-id="fabeb-159">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="fabeb-159">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fabeb-160">輸出</span><span class="sxs-lookup"><span data-stu-id="fabeb-160">OUTPUTS</span></span>

### <span data-ttu-id="fabeb-161">System.object</span><span class="sxs-lookup"><span data-stu-id="fabeb-161">System.String</span></span>

## <span data-ttu-id="fabeb-162">筆記</span><span class="sxs-lookup"><span data-stu-id="fabeb-162">NOTES</span></span>

## <span data-ttu-id="fabeb-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="fabeb-163">RELATED LINKS</span></span>

[<span data-ttu-id="fabeb-164">移除-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="fabeb-164">Remove-AzApiManagementPolicy</span></span>](./Remove-AzApiManagementPolicy.md)

[<span data-ttu-id="fabeb-165">Set-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="fabeb-165">Set-AzApiManagementPolicy</span></span>](./Set-AzApiManagementPolicy.md)


