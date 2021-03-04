---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 7BCEB0EF-1A09-4CED-9F34-CE3AB03181A7
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementPolicy.md
ms.openlocfilehash: dbabc98a8221cc2b870368b2b9cdd55e81280863
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912941"
---
# <span data-ttu-id="a14e4-101">Get-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="a14e4-101">Get-AzApiManagementPolicy</span></span>

## <span data-ttu-id="a14e4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a14e4-102">SYNOPSIS</span></span>
<span data-ttu-id="a14e4-103">獲得指定的範圍策略。</span><span class="sxs-lookup"><span data-stu-id="a14e4-103">Gets the specified scope policy.</span></span>

## <span data-ttu-id="a14e4-104">語法</span><span class="sxs-lookup"><span data-stu-id="a14e4-104">SYNTAX</span></span>

### <span data-ttu-id="a14e4-105">GetTenantLevel (預設) </span><span class="sxs-lookup"><span data-stu-id="a14e4-105">GetTenantLevel (Default)</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a14e4-106">GetProductLevel</span><span class="sxs-lookup"><span data-stu-id="a14e4-106">GetProductLevel</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ProductId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a14e4-107">GetApiLevel</span><span class="sxs-lookup"><span data-stu-id="a14e4-107">GetApiLevel</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-ApiRevision <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a14e4-108">GetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="a14e4-108">GetOperationLevel</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-ApiRevision <String>] -OperationId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a14e4-109">描述</span><span class="sxs-lookup"><span data-stu-id="a14e4-109">DESCRIPTION</span></span>
<span data-ttu-id="a14e4-110">**Get-AzApiManagementPolidlet** 會取得指定的範圍策略。</span><span class="sxs-lookup"><span data-stu-id="a14e4-110">The **Get-AzApiManagementPolicy** cmdlet gets the specified scope policy.</span></span>

## <span data-ttu-id="a14e4-111">例子</span><span class="sxs-lookup"><span data-stu-id="a14e4-111">EXAMPLES</span></span>

### <span data-ttu-id="a14e4-112">範例 1：取得租使用者層級策略</span><span class="sxs-lookup"><span data-stu-id="a14e4-112">Example 1: Get the tenant level policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -SaveAs "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="a14e4-113">此命令會獲得租使用者層級策略，並存到名為 tenantpolicy.xml。</span><span class="sxs-lookup"><span data-stu-id="a14e4-113">This command gets tenant level policy and saves it to a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="a14e4-114">範例 2：取得產品範圍策略</span><span class="sxs-lookup"><span data-stu-id="a14e4-114">Example 2: Get the product-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="a14e4-115">此命令會獲得產品範圍策略</span><span class="sxs-lookup"><span data-stu-id="a14e4-115">This command gets product-scope policy</span></span>

### <span data-ttu-id="a14e4-116">範例 3：取得 API 範圍策略</span><span class="sxs-lookup"><span data-stu-id="a14e4-116">Example 3: Get the API-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

<span data-ttu-id="a14e4-117">此命令會獲得 API 範圍策略。</span><span class="sxs-lookup"><span data-stu-id="a14e4-117">This command gets API-scope policy.</span></span>

### <span data-ttu-id="a14e4-118">範例 4：取得作業範圍策略</span><span class="sxs-lookup"><span data-stu-id="a14e4-118">Example 4: Get the operation-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="a14e4-119">此命令會獲得作業範圍策略。</span><span class="sxs-lookup"><span data-stu-id="a14e4-119">This command gets the operation-scope policy.</span></span>

### <span data-ttu-id="a14e4-120">範例 5：以 RawXml 格式取得租使用者範圍策略</span><span class="sxs-lookup"><span data-stu-id="a14e4-120">Example 5: Get the Tenant scope policy in RawXml format</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS c:\> Get-AzApiManagementPolicy -Context $apimContext -Format rawxml

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

<span data-ttu-id="a14e4-121">此命令會以非 Xml 逸出格式獲得租使用者範圍策略。</span><span class="sxs-lookup"><span data-stu-id="a14e4-121">This command gets the tenant-scope policy in Non-Xml escaped format.</span></span>

## <span data-ttu-id="a14e4-122">參數</span><span class="sxs-lookup"><span data-stu-id="a14e4-122">PARAMETERS</span></span>

### <span data-ttu-id="a14e4-123">-ApiId</span><span class="sxs-lookup"><span data-stu-id="a14e4-123">-ApiId</span></span>
<span data-ttu-id="a14e4-124">指定現有 API 的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a14e4-124">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="a14e4-125">如果您指定此參數，Cmdlet 會返回 API 範圍策略。</span><span class="sxs-lookup"><span data-stu-id="a14e4-125">If you specify this parameter the cmdlet returns the API-scope policy.</span></span>

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

### <span data-ttu-id="a14e4-126">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="a14e4-126">-ApiRevision</span></span>
<span data-ttu-id="a14e4-127">API 修訂的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a14e4-127">Identifier of API Revision.</span></span> <span data-ttu-id="a14e4-128">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="a14e4-128">This parameter is optional.</span></span> <span data-ttu-id="a14e4-129">如果未指定，將會從目前使用中的 api 修訂中取回該規則。</span><span class="sxs-lookup"><span data-stu-id="a14e4-129">If not specified, the policy will be retrieved from the currently active api revision.</span></span>

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

### <span data-ttu-id="a14e4-130">-內容</span><span class="sxs-lookup"><span data-stu-id="a14e4-130">-Context</span></span>
<span data-ttu-id="a14e4-131">指定 **PsApiManagementCoNtext 的實例**。</span><span class="sxs-lookup"><span data-stu-id="a14e4-131">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="a14e4-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a14e4-132">-DefaultProfile</span></span>
<span data-ttu-id="a14e4-133">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a14e4-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a14e4-134">-強制</span><span class="sxs-lookup"><span data-stu-id="a14e4-134">-Force</span></span>
<span data-ttu-id="a14e4-135">ps_force</span><span class="sxs-lookup"><span data-stu-id="a14e4-135">ps_force</span></span>

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

### <span data-ttu-id="a14e4-136">-格式</span><span class="sxs-lookup"><span data-stu-id="a14e4-136">-Format</span></span>
<span data-ttu-id="a14e4-137">指定 API 管理原則的格式。</span><span class="sxs-lookup"><span data-stu-id="a14e4-137">Specifies the format of the API management policy.</span></span>
<span data-ttu-id="a14e4-138">此參數的預設值為 "xml"。</span><span class="sxs-lookup"><span data-stu-id="a14e4-138">The default value for this parameter is "xml".</span></span>

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

### <span data-ttu-id="a14e4-139">-OperationId</span><span class="sxs-lookup"><span data-stu-id="a14e4-139">-OperationId</span></span>
<span data-ttu-id="a14e4-140">指定現有 API 作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a14e4-140">Specifies the identifier of the existing API operation.</span></span>
<span data-ttu-id="a14e4-141">如果您使用 *ApiId* 指定此參數，Cmdlet 會返回作業範圍策略。</span><span class="sxs-lookup"><span data-stu-id="a14e4-141">If you specify this parameter with *ApiId* the cmdlet returns operation-scope policy.</span></span>

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

### <span data-ttu-id="a14e4-142">-ProductId</span><span class="sxs-lookup"><span data-stu-id="a14e4-142">-ProductId</span></span>
<span data-ttu-id="a14e4-143">指定現有產品的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a14e4-143">Specifies the identifier of an existing product.</span></span>
<span data-ttu-id="a14e4-144">如果您指定此參數，Cmdlet 會返回產品範圍策略。</span><span class="sxs-lookup"><span data-stu-id="a14e4-144">If you specify this parameter the cmdlet returns the product-scope policy.</span></span>

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

### <span data-ttu-id="a14e4-145">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="a14e4-145">-SaveAs</span></span>
<span data-ttu-id="a14e4-146">指定要儲存結果的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="a14e4-146">Specifies the file path to save the result to.</span></span>
<span data-ttu-id="a14e4-147">如果您未指定此參數，則結果會以 sting 為管道。</span><span class="sxs-lookup"><span data-stu-id="a14e4-147">If you do not specify this parameter the result is pipelined as a sting.</span></span>

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

### <span data-ttu-id="a14e4-148">-確認</span><span class="sxs-lookup"><span data-stu-id="a14e4-148">-Confirm</span></span>
<span data-ttu-id="a14e4-149">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a14e4-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a14e4-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a14e4-150">-WhatIf</span></span>
<span data-ttu-id="a14e4-151">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a14e4-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a14e4-152">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a14e4-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a14e4-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a14e4-153">CommonParameters</span></span>
<span data-ttu-id="a14e4-154">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a14e4-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a14e4-155">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a14e4-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a14e4-156">輸入</span><span class="sxs-lookup"><span data-stu-id="a14e4-156">INPUTS</span></span>

### <span data-ttu-id="a14e4-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="a14e4-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a14e4-158">System.String</span><span class="sxs-lookup"><span data-stu-id="a14e4-158">System.String</span></span>

### <span data-ttu-id="a14e4-159">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a14e4-159">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a14e4-160">輸出</span><span class="sxs-lookup"><span data-stu-id="a14e4-160">OUTPUTS</span></span>

### <span data-ttu-id="a14e4-161">System.String</span><span class="sxs-lookup"><span data-stu-id="a14e4-161">System.String</span></span>

## <span data-ttu-id="a14e4-162">筆記</span><span class="sxs-lookup"><span data-stu-id="a14e4-162">NOTES</span></span>

## <span data-ttu-id="a14e4-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="a14e4-163">RELATED LINKS</span></span>

[<span data-ttu-id="a14e4-164">Remove-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="a14e4-164">Remove-AzApiManagementPolicy</span></span>](./Remove-AzApiManagementPolicy.md)

[<span data-ttu-id="a14e4-165">Set-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="a14e4-165">Set-AzApiManagementPolicy</span></span>](./Set-AzApiManagementPolicy.md)


