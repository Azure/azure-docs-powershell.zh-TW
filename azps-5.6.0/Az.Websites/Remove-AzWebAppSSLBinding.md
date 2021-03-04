---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3AB3D398-E5DB-4214-BA27-6E3B7D
online version: https://docs.microsoft.com/powershell/module/az.websites/remove-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSSLBinding.md
ms.openlocfilehash: b1d9aa1f212ce31a8bb7fadeff4e0ca8afcf05e0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903750"
---
# <span data-ttu-id="fd8c1-101">Remove-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="fd8c1-101">Remove-AzWebAppSSLBinding</span></span>

## <span data-ttu-id="fd8c1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="fd8c1-102">SYNOPSIS</span></span>
<span data-ttu-id="fd8c1-103">從上傳的憑證移除 SSL 綁定。</span><span class="sxs-lookup"><span data-stu-id="fd8c1-103">Removes an SSL binding from an uploaded certificate.</span></span>

## <span data-ttu-id="fd8c1-104">語法</span><span class="sxs-lookup"><span data-stu-id="fd8c1-104">SYNTAX</span></span>

### <span data-ttu-id="fd8c1-105">S1</span><span class="sxs-lookup"><span data-stu-id="fd8c1-105">S1</span></span>
```
Remove-AzWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force]
 [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd8c1-106">S2</span><span class="sxs-lookup"><span data-stu-id="fd8c1-106">S2</span></span>
```
Remove-AzWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd8c1-107">描述</span><span class="sxs-lookup"><span data-stu-id="fd8c1-107">DESCRIPTION</span></span>
<span data-ttu-id="fd8c1-108">**Remove-AzWebAppSSLBinding** Cmdlet 會從 Azure Web App 移除安全通訊端層 (SSL) 綁定。</span><span class="sxs-lookup"><span data-stu-id="fd8c1-108">The **Remove-AzWebAppSSLBinding** cmdlet removes a Secure Sockets Layer (SSL) binding from an Azure Web App.</span></span>
<span data-ttu-id="fd8c1-109">SSL 系裝訂可用來將 Web App 與憑證關聯。</span><span class="sxs-lookup"><span data-stu-id="fd8c1-109">SSL bindings are used to associate a Web App with a certificate.</span></span>

## <span data-ttu-id="fd8c1-110">例子</span><span class="sxs-lookup"><span data-stu-id="fd8c1-110">EXAMPLES</span></span>

### <span data-ttu-id="fd8c1-111">範例 1：移除 Web App 的 SSL 綁定</span><span class="sxs-lookup"><span data-stu-id="fd8c1-111">Example 1: Remove an SSL binding for a web app</span></span>
```
PS C:\>Remove-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com"
```

<span data-ttu-id="fd8c1-112">此命令會移除 Web App ContosoWebApp 的 SSL 綁定。</span><span class="sxs-lookup"><span data-stu-id="fd8c1-112">This command removes the SSL binding for the web app ContosoWebApp.</span></span>
<span data-ttu-id="fd8c1-113">由於 *DeleteCertificate* 參數不包含在內，如果憑證不再具有任何 SSL 綁定，將會刪除該憑證。</span><span class="sxs-lookup"><span data-stu-id="fd8c1-113">Since the *DeleteCertificate* parameter is not included, the certificate will be deleted if it no longer has any SSL bindings.</span></span>

### <span data-ttu-id="fd8c1-114">範例 2：移除 SSL 綁定而不移除憑證</span><span class="sxs-lookup"><span data-stu-id="fd8c1-114">Example 2: Remove an SSL binding without removing the certificate</span></span>
```
PS C:\>Remove-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com" -DeleteCertificate $False
```

<span data-ttu-id="fd8c1-115">與範例 1 類似，此命令也會移除 Web App ContosoWebApp 的 SSL 綁定。</span><span class="sxs-lookup"><span data-stu-id="fd8c1-115">Similar to Example 1, this command also removes the SSL binding for the Web App ContosoWebApp.</span></span>
<span data-ttu-id="fd8c1-116">不過，在此案例中，會包含 *DeleteCertificate* 參數，參數值會設為 $False。</span><span class="sxs-lookup"><span data-stu-id="fd8c1-116">In this case, however, the *DeleteCertificate* parameter is included, and the parameter value is set to $False.</span></span>
<span data-ttu-id="fd8c1-117">這表示無論憑證是否具有任何 SSL 綁定，都將不會刪除。</span><span class="sxs-lookup"><span data-stu-id="fd8c1-117">That means that the certificate will not be deleted regardless of whether it has any SSL bindings or not.</span></span>

### <span data-ttu-id="fd8c1-118">範例 3：使用物件參照移除 SSL 綁定</span><span class="sxs-lookup"><span data-stu-id="fd8c1-118">Example 3: Use an object reference to remove an SSL binding</span></span>
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Remove-AzWebAppSSLBinding -WebApp $WebApp -Name "www.contoso.com"
```

<span data-ttu-id="fd8c1-119">此範例使用對 Web App 網站的物件參照來移除 Web App 的 SSL 綁定。</span><span class="sxs-lookup"><span data-stu-id="fd8c1-119">This example uses an object reference to the Web App website to remove the SSL binding for a Web App.</span></span>
<span data-ttu-id="fd8c1-120">第一個命令使用 Get-AzWebApp Cmdlet 建立名為 ContosoWebApp 的 Web App 物件參照。</span><span class="sxs-lookup"><span data-stu-id="fd8c1-120">The first command uses the Get-AzWebApp cmdlet to create an object reference to the Web App named ContosoWebApp.</span></span>
<span data-ttu-id="fd8c1-121">該物件參照會儲存在名為 $WebApp 的變數中。</span><span class="sxs-lookup"><span data-stu-id="fd8c1-121">That object reference is stored in a variable named $WebApp.</span></span>
<span data-ttu-id="fd8c1-122">第二個命令使用物件參照和 **Remove-AzWebAppSSLBinding** Cmdlet 來移除 SSL 綁定。</span><span class="sxs-lookup"><span data-stu-id="fd8c1-122">The second command uses the object reference and the **Remove-AzWebAppSSLBinding** cmdlet to remove the SSL binding.</span></span>

## <span data-ttu-id="fd8c1-123">參數</span><span class="sxs-lookup"><span data-stu-id="fd8c1-123">PARAMETERS</span></span>

### <span data-ttu-id="fd8c1-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd8c1-124">-DefaultProfile</span></span>
<span data-ttu-id="fd8c1-125">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="fd8c1-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd8c1-126">-DeleteCertificate</span><span class="sxs-lookup"><span data-stu-id="fd8c1-126">-DeleteCertificate</span></span>
<span data-ttu-id="fd8c1-127">指定移除 SSL 綁定時要採取的動作，這是憑證使用的唯一綁定。</span><span class="sxs-lookup"><span data-stu-id="fd8c1-127">Specifies the action to take place if the SSL binding being removed is the only binding used by the certificate.</span></span>
<span data-ttu-id="fd8c1-128">如果 *DeleteCertificate* 設定為 $False，則刪除綁定時不會刪除憑證。</span><span class="sxs-lookup"><span data-stu-id="fd8c1-128">If *DeleteCertificate* is set to $False, the certificate will not be deleted when the binding is deleted.</span></span>
<span data-ttu-id="fd8c1-129">如果 *DeleteCertificate* 設定為 $True或不包含在命令中，憑證會連同 SSL 綁定一起刪除。</span><span class="sxs-lookup"><span data-stu-id="fd8c1-129">If *DeleteCertificate* is set to $True or is not included in the command, the certificate will be deleted along with the SSL binding.</span></span>
<span data-ttu-id="fd8c1-130">只有在要移除的 SSL 綁定是憑證使用的唯一綁定時，憑證才能刪除。</span><span class="sxs-lookup"><span data-stu-id="fd8c1-130">The certificate will only be deleted if the SSL binding being removed is the only binding used by the certificate.</span></span>
<span data-ttu-id="fd8c1-131">如果憑證具有一種以上裝訂，無論 *DeleteCertificate* 參數的值如何，都將不會移除憑證。</span><span class="sxs-lookup"><span data-stu-id="fd8c1-131">If the certificate has more than one binding, the certificate will not be removed regardless of the value of the *DeleteCertificate* parameter.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd8c1-132">-強制</span><span class="sxs-lookup"><span data-stu-id="fd8c1-132">-Force</span></span>
<span data-ttu-id="fd8c1-133">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="fd8c1-133">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd8c1-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="fd8c1-134">-Name</span></span>
<span data-ttu-id="fd8c1-135">指定 Web App 的名稱。</span><span class="sxs-lookup"><span data-stu-id="fd8c1-135">Specifies the name of the Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd8c1-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd8c1-136">-ResourceGroupName</span></span>
<span data-ttu-id="fd8c1-137">指定憑證指派給的資源組名。</span><span class="sxs-lookup"><span data-stu-id="fd8c1-137">Specifies the name of the resource group that the certificate is assigned to.</span></span>
<span data-ttu-id="fd8c1-138">您無法在同一 *個命令中使用 ResourceGroupName* 參數和 *WebApp* 參數。</span><span class="sxs-lookup"><span data-stu-id="fd8c1-138">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd8c1-139">-Slot</span><span class="sxs-lookup"><span data-stu-id="fd8c1-139">-Slot</span></span>
<span data-ttu-id="fd8c1-140">指定 Web App 部署插槽。</span><span class="sxs-lookup"><span data-stu-id="fd8c1-140">Specifies the Web App deployment slot.</span></span>
<span data-ttu-id="fd8c1-141">若要取得部署插槽，請使用 Get-AzWebAppSlot Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fd8c1-141">To get a deployment slot, use the Get-AzWebAppSlot cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd8c1-142">-WebApp</span><span class="sxs-lookup"><span data-stu-id="fd8c1-142">-WebApp</span></span>
<span data-ttu-id="fd8c1-143">指定 Web App。</span><span class="sxs-lookup"><span data-stu-id="fd8c1-143">Specifies a Web App.</span></span>
<span data-ttu-id="fd8c1-144">若要取得 Web App，請使用 Get-AzWebApp Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fd8c1-144">To get a Web App, use the Get-AzWebApp cmdlet.</span></span>
<span data-ttu-id="fd8c1-145">您無法在 *ResourceGroupName* 參數和/或 *WebAppName* 的相同命令中，使用 WebApp 參數。 </span><span class="sxs-lookup"><span data-stu-id="fd8c1-145">You cannot use the *WebApp* parameter in the same command as the *ResourceGroupName* parameter and/or the *WebAppName*.</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd8c1-146">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="fd8c1-146">-WebAppName</span></span>
<span data-ttu-id="fd8c1-147">指定 Web App 的名稱。</span><span class="sxs-lookup"><span data-stu-id="fd8c1-147">Specifies the name of the Web App.</span></span>
<span data-ttu-id="fd8c1-148">您無法在同一個命令中使用 *WebAppName* 參數和 *WebApp* 參數。</span><span class="sxs-lookup"><span data-stu-id="fd8c1-148">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd8c1-149">-確認</span><span class="sxs-lookup"><span data-stu-id="fd8c1-149">-Confirm</span></span>
<span data-ttu-id="fd8c1-150">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="fd8c1-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd8c1-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd8c1-151">-WhatIf</span></span>
<span data-ttu-id="fd8c1-152">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fd8c1-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd8c1-153">不會執行 Cmdlet。顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fd8c1-153">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd8c1-154">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fd8c1-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd8c1-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd8c1-155">CommonParameters</span></span>
<span data-ttu-id="fd8c1-156">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="fd8c1-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd8c1-157">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="fd8c1-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd8c1-158">輸入</span><span class="sxs-lookup"><span data-stu-id="fd8c1-158">INPUTS</span></span>

### <span data-ttu-id="fd8c1-159">Microsoft.Azure.Commands.WebApps.models.PSSite</span><span class="sxs-lookup"><span data-stu-id="fd8c1-159">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="fd8c1-160">輸出</span><span class="sxs-lookup"><span data-stu-id="fd8c1-160">OUTPUTS</span></span>

### <span data-ttu-id="fd8c1-161">System.Void</span><span class="sxs-lookup"><span data-stu-id="fd8c1-161">System.Void</span></span>

## <span data-ttu-id="fd8c1-162">筆記</span><span class="sxs-lookup"><span data-stu-id="fd8c1-162">NOTES</span></span>

## <span data-ttu-id="fd8c1-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="fd8c1-163">RELATED LINKS</span></span>

[<span data-ttu-id="fd8c1-164">Get-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="fd8c1-164">Get-AzWebAppSSLBinding</span></span>](./Get-AzWebAppSSLBinding.md)

[<span data-ttu-id="fd8c1-165">New-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="fd8c1-165">New-AzWebAppSSLBinding</span></span>](./New-AzWebAppSSLBinding.md)

[<span data-ttu-id="fd8c1-166">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fd8c1-166">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="fd8c1-167">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="fd8c1-167">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


