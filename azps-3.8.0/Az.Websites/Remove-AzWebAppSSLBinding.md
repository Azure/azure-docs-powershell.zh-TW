---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3AB3D398-E5DB-4214-BA27-6E3B7D225550
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSSLBinding.md
ms.openlocfilehash: bed5cb961fd39975b3f10debe8791a418fd5dcda
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958862"
---
# <span data-ttu-id="cf0c2-101">Remove-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="cf0c2-101">Remove-AzWebAppSSLBinding</span></span>

## <span data-ttu-id="cf0c2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cf0c2-102">SYNOPSIS</span></span>
<span data-ttu-id="cf0c2-103">從上傳的憑證中移除 SSL 系結。</span><span class="sxs-lookup"><span data-stu-id="cf0c2-103">Removes an SSL binding from an uploaded certificate.</span></span>

## <span data-ttu-id="cf0c2-104">句法</span><span class="sxs-lookup"><span data-stu-id="cf0c2-104">SYNTAX</span></span>

### <span data-ttu-id="cf0c2-105">S1</span><span class="sxs-lookup"><span data-stu-id="cf0c2-105">S1</span></span>
```
Remove-AzWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force]
 [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf0c2-106">S2</span><span class="sxs-lookup"><span data-stu-id="cf0c2-106">S2</span></span>
```
Remove-AzWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf0c2-107">說明</span><span class="sxs-lookup"><span data-stu-id="cf0c2-107">DESCRIPTION</span></span>
<span data-ttu-id="cf0c2-108">**AzWebAppSSLBinding** Cmdlet 會從 Azure Web APP (SSL) 系結來移除安全通訊端層。</span><span class="sxs-lookup"><span data-stu-id="cf0c2-108">The **Remove-AzWebAppSSLBinding** cmdlet removes a Secure Sockets Layer (SSL) binding from an Azure Web App.</span></span>
<span data-ttu-id="cf0c2-109">SSL 系結是用來將 Web App 與憑證建立關聯。</span><span class="sxs-lookup"><span data-stu-id="cf0c2-109">SSL bindings are used to associate a Web App with a certificate.</span></span>

## <span data-ttu-id="cf0c2-110">示例</span><span class="sxs-lookup"><span data-stu-id="cf0c2-110">EXAMPLES</span></span>

### <span data-ttu-id="cf0c2-111">範例1：移除 web 應用程式的 SSL 系結</span><span class="sxs-lookup"><span data-stu-id="cf0c2-111">Example 1: Remove an SSL binding for a web app</span></span>
```
PS C:\>Remove-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com"
```

<span data-ttu-id="cf0c2-112">這個命令會移除 web 應用程式 ContosoWebApp 的 SSL 系結。</span><span class="sxs-lookup"><span data-stu-id="cf0c2-112">This command removes the SSL binding for the web app ContosoWebApp.</span></span>
<span data-ttu-id="cf0c2-113">由於不包含 *DeleteCertificate* 參數，因此如果證書不再有任何 SSL 系結，就會將它刪除。</span><span class="sxs-lookup"><span data-stu-id="cf0c2-113">Since the *DeleteCertificate* parameter is not included, the certificate will be deleted if it no longer has any SSL bindings.</span></span>

### <span data-ttu-id="cf0c2-114">範例2：移除 SSL 系結但不移除憑證</span><span class="sxs-lookup"><span data-stu-id="cf0c2-114">Example 2: Remove an SSL binding without removing the certificate</span></span>
```
PS C:\>Remove-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com" -DeleteCertificate $False
```

<span data-ttu-id="cf0c2-115">與範例1類似，這個命令也會移除 Web App ContosoWebApp 的 SSL 系結。</span><span class="sxs-lookup"><span data-stu-id="cf0c2-115">Similar to Example 1, this command also removes the SSL binding for the Web App ContosoWebApp.</span></span>
<span data-ttu-id="cf0c2-116">但在此情況下，會包含 *DeleteCertificate* 參數，而參數值會設定為 $False。</span><span class="sxs-lookup"><span data-stu-id="cf0c2-116">In this case, however, the *DeleteCertificate* parameter is included, and the parameter value is set to $False.</span></span>
<span data-ttu-id="cf0c2-117">這表示無論是否有任何 SSL 綁定，證書都不會被刪除。</span><span class="sxs-lookup"><span data-stu-id="cf0c2-117">That means that the certificate will not be deleted regardless of whether it has any SSL bindings or not.</span></span>

### <span data-ttu-id="cf0c2-118">範例3：使用物件參照來移除 SSL 系結</span><span class="sxs-lookup"><span data-stu-id="cf0c2-118">Example 3: Use an object reference to remove an SSL binding</span></span>
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Remove-AzWebAppSSLBinding -WebApp $WebApp -Name "www.contoso.com"
```

<span data-ttu-id="cf0c2-119">這個範例使用 Web App 網站的物件參考來移除 Web 應用程式的 SSL 系結。</span><span class="sxs-lookup"><span data-stu-id="cf0c2-119">This example uses an object reference to the Web App website to remove the SSL binding for a Web App.</span></span>
<span data-ttu-id="cf0c2-120">第一個命令使用 Get-AzWebApp Cmdlet 來建立名為 ContosoWebApp 的 Web App 的物件參考。</span><span class="sxs-lookup"><span data-stu-id="cf0c2-120">The first command uses the Get-AzWebApp cmdlet to create an object reference to the Web App named ContosoWebApp.</span></span>
<span data-ttu-id="cf0c2-121">該物件參照會儲存在名為 $WebApp 的變數中。</span><span class="sxs-lookup"><span data-stu-id="cf0c2-121">That object reference is stored in a variable named $WebApp.</span></span>
<span data-ttu-id="cf0c2-122">第二個命令使用物件參照和 **AzWebAppSSLBinding** Cmdlet 來移除 SSL 系結。</span><span class="sxs-lookup"><span data-stu-id="cf0c2-122">The second command uses the object reference and the **Remove-AzWebAppSSLBinding** cmdlet to remove the SSL binding.</span></span>

## <span data-ttu-id="cf0c2-123">參數</span><span class="sxs-lookup"><span data-stu-id="cf0c2-123">PARAMETERS</span></span>

### <span data-ttu-id="cf0c2-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf0c2-124">-DefaultProfile</span></span>
<span data-ttu-id="cf0c2-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cf0c2-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf0c2-126">-DeleteCertificate</span><span class="sxs-lookup"><span data-stu-id="cf0c2-126">-DeleteCertificate</span></span>
<span data-ttu-id="cf0c2-127">指定在移除 SSL 系結是憑證所使用的唯一系結時要發生的動作。</span><span class="sxs-lookup"><span data-stu-id="cf0c2-127">Specifies the action to take place if the SSL binding being removed is the only binding used by the certificate.</span></span>
<span data-ttu-id="cf0c2-128">如果 *DeleteCertificate* 設定為 $False，則刪除系結時，不會刪除憑證。</span><span class="sxs-lookup"><span data-stu-id="cf0c2-128">If *DeleteCertificate* is set to $False, the certificate will not be deleted when the binding is deleted.</span></span>
<span data-ttu-id="cf0c2-129">如果 *DeleteCertificate* 設定為 $True 或不包含在命令中，則會將憑證與 SSL 系結一起刪除。</span><span class="sxs-lookup"><span data-stu-id="cf0c2-129">If *DeleteCertificate* is set to $True or is not included in the command, the certificate will be deleted along with the SSL binding.</span></span>
<span data-ttu-id="cf0c2-130">只有在已移除 SSL 系結是認證所使用的唯一系結時，才能刪除證書。</span><span class="sxs-lookup"><span data-stu-id="cf0c2-130">The certificate will only be deleted if the SSL binding being removed is the only binding used by the certificate.</span></span>
<span data-ttu-id="cf0c2-131">如果憑證有一個以上的系結，不論 *DeleteCertificate* 參數的值為何，都不會移除證書。</span><span class="sxs-lookup"><span data-stu-id="cf0c2-131">If the certificate has more than one binding, the certificate will not be removed regardless of the value of the *DeleteCertificate* parameter.</span></span>

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

### <span data-ttu-id="cf0c2-132">-Force</span><span class="sxs-lookup"><span data-stu-id="cf0c2-132">-Force</span></span>
<span data-ttu-id="cf0c2-133">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="cf0c2-133">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cf0c2-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="cf0c2-134">-Name</span></span>
<span data-ttu-id="cf0c2-135">指定 Web 應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="cf0c2-135">Specifies the name of the Web App.</span></span>

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

### <span data-ttu-id="cf0c2-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf0c2-136">-ResourceGroupName</span></span>
<span data-ttu-id="cf0c2-137">指定指派憑證的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cf0c2-137">Specifies the name of the resource group that the certificate is assigned to.</span></span>
<span data-ttu-id="cf0c2-138">您無法在同一命令中使用 *ResourceGroupName* 參數和 *WebApp* 參數。</span><span class="sxs-lookup"><span data-stu-id="cf0c2-138">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="cf0c2-139">-槽</span><span class="sxs-lookup"><span data-stu-id="cf0c2-139">-Slot</span></span>
<span data-ttu-id="cf0c2-140">指定 Web 應用程式部署槽。</span><span class="sxs-lookup"><span data-stu-id="cf0c2-140">Specifies the Web App deployment slot.</span></span>
<span data-ttu-id="cf0c2-141">若要取得部署槽，請使用 Get-AzWebAppSlot Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cf0c2-141">To get a deployment slot, use the Get-AzWebAppSlot cmdlet.</span></span>

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

### <span data-ttu-id="cf0c2-142">-WebApp</span><span class="sxs-lookup"><span data-stu-id="cf0c2-142">-WebApp</span></span>
<span data-ttu-id="cf0c2-143">指定 Web 應用程式。</span><span class="sxs-lookup"><span data-stu-id="cf0c2-143">Specifies a Web App.</span></span>
<span data-ttu-id="cf0c2-144">若要取得 Web 應用程式，請使用 Get-AzWebApp Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cf0c2-144">To get a Web App, use the Get-AzWebApp cmdlet.</span></span>
<span data-ttu-id="cf0c2-145">您無法在與 *ResourceGroupName* 參數和/或 *WebAppName* 相同的命令中使用 *WebApp* 參數。</span><span class="sxs-lookup"><span data-stu-id="cf0c2-145">You cannot use the *WebApp* parameter in the same command as the *ResourceGroupName* parameter and/or the *WebAppName*.</span></span>

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

### <span data-ttu-id="cf0c2-146">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="cf0c2-146">-WebAppName</span></span>
<span data-ttu-id="cf0c2-147">指定 Web 應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="cf0c2-147">Specifies the name of the Web App.</span></span>
<span data-ttu-id="cf0c2-148">您無法在同一命令中使用 *WebAppName* 參數和 *WebApp* 參數。</span><span class="sxs-lookup"><span data-stu-id="cf0c2-148">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="cf0c2-149">-確認</span><span class="sxs-lookup"><span data-stu-id="cf0c2-149">-Confirm</span></span>
<span data-ttu-id="cf0c2-150">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cf0c2-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf0c2-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf0c2-151">-WhatIf</span></span>
<span data-ttu-id="cf0c2-152">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cf0c2-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf0c2-153">未執行 Cmdlet。顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cf0c2-153">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf0c2-154">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cf0c2-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf0c2-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf0c2-155">CommonParameters</span></span>
<span data-ttu-id="cf0c2-156">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cf0c2-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf0c2-157">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cf0c2-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf0c2-158">輸入</span><span class="sxs-lookup"><span data-stu-id="cf0c2-158">INPUTS</span></span>

### <span data-ttu-id="cf0c2-159">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="cf0c2-159">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="cf0c2-160">輸出</span><span class="sxs-lookup"><span data-stu-id="cf0c2-160">OUTPUTS</span></span>

### <span data-ttu-id="cf0c2-161">System.void</span><span class="sxs-lookup"><span data-stu-id="cf0c2-161">System.Void</span></span>

## <span data-ttu-id="cf0c2-162">筆記</span><span class="sxs-lookup"><span data-stu-id="cf0c2-162">NOTES</span></span>

## <span data-ttu-id="cf0c2-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="cf0c2-163">RELATED LINKS</span></span>

[<span data-ttu-id="cf0c2-164">AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="cf0c2-164">Get-AzWebAppSSLBinding</span></span>](./Get-AzWebAppSSLBinding.md)

[<span data-ttu-id="cf0c2-165">新-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="cf0c2-165">New-AzWebAppSSLBinding</span></span>](./New-AzWebAppSSLBinding.md)

[<span data-ttu-id="cf0c2-166">AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="cf0c2-166">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="cf0c2-167">AzWebApp</span><span class="sxs-lookup"><span data-stu-id="cf0c2-167">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


