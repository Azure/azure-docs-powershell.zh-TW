---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 3AB3D398-E5DB-4214-BA27-6E3B7D225550
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermwebappsslbinding
schema: 2.0.0
ms.openlocfilehash: 06bb13207a666b4537c267e391818865e4165e74
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93799705"
---
# <span data-ttu-id="77684-101">Remove-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="77684-101">Remove-AzureRmWebAppSSLBinding</span></span>

## <span data-ttu-id="77684-102">摘要</span><span class="sxs-lookup"><span data-stu-id="77684-102">SYNOPSIS</span></span>
<span data-ttu-id="77684-103">從上傳的憑證中移除 SSL 系結。</span><span class="sxs-lookup"><span data-stu-id="77684-103">Removes an SSL binding from an uploaded certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77684-104">句法</span><span class="sxs-lookup"><span data-stu-id="77684-104">SYNTAX</span></span>

### <span data-ttu-id="77684-105">S1</span><span class="sxs-lookup"><span data-stu-id="77684-105">S1</span></span>
```
Remove-AzureRmWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force]
 [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77684-106">S2</span><span class="sxs-lookup"><span data-stu-id="77684-106">S2</span></span>
```
Remove-AzureRmWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77684-107">說明</span><span class="sxs-lookup"><span data-stu-id="77684-107">DESCRIPTION</span></span>
<span data-ttu-id="77684-108">**AzureRmWebAppSSLBinding** Cmdlet 會從 Azure Web APP (SSL) 系結來移除安全通訊端層。</span><span class="sxs-lookup"><span data-stu-id="77684-108">The **Remove-AzureRmWebAppSSLBinding** cmdlet removes a Secure Sockets Layer (SSL) binding from an Azure Web App.</span></span>
<span data-ttu-id="77684-109">SSL 系結是用來將 Web App 與憑證建立關聯。</span><span class="sxs-lookup"><span data-stu-id="77684-109">SSL bindings are used to associate a Web App with a certificate.</span></span>

## <span data-ttu-id="77684-110">示例</span><span class="sxs-lookup"><span data-stu-id="77684-110">EXAMPLES</span></span>

### <span data-ttu-id="77684-111">範例1：移除 web 應用程式的 SSL 系結</span><span class="sxs-lookup"><span data-stu-id="77684-111">Example 1: Remove an SSL binding for a web app</span></span>
```
PS C:\>Remove-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com"
```

<span data-ttu-id="77684-112">這個命令會移除 web 應用程式 ContosoWebApp 的 SSL 系結。</span><span class="sxs-lookup"><span data-stu-id="77684-112">This command removes the SSL binding for the web app ContosoWebApp.</span></span>
<span data-ttu-id="77684-113">由於不包含 *DeleteCertificate* 參數，因此如果證書不再有任何 SSL 系結，就會將它刪除。</span><span class="sxs-lookup"><span data-stu-id="77684-113">Since the *DeleteCertificate* parameter is not included, the certificate will be deleted if it no longer has any SSL bindings.</span></span>

### <span data-ttu-id="77684-114">範例2：移除 SSL 系結但不移除憑證</span><span class="sxs-lookup"><span data-stu-id="77684-114">Example 2: Remove an SSL binding without removing the certificate</span></span>
```
PS C:\>Remove-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com" -DeleteCertificate $False
```

<span data-ttu-id="77684-115">與範例1類似，這個命令也會移除 Web App ContosoWebApp 的 SSL 系結。</span><span class="sxs-lookup"><span data-stu-id="77684-115">Similar to Example 1, this command also removes the SSL binding for the Web App ContosoWebApp.</span></span>
<span data-ttu-id="77684-116">但在此情況下，會包含 *DeleteCertificate* 參數，而參數值會設定為 $False。</span><span class="sxs-lookup"><span data-stu-id="77684-116">In this case, however, the *DeleteCertificate* parameter is included, and the parameter value is set to $False.</span></span>
<span data-ttu-id="77684-117">這表示無論是否有任何 SSL 綁定，證書都不會被刪除。</span><span class="sxs-lookup"><span data-stu-id="77684-117">That means that the certificate will not be deleted regardless of whether it has any SSL bindings or not.</span></span>

### <span data-ttu-id="77684-118">範例3：使用物件參照來移除 SSL 系結</span><span class="sxs-lookup"><span data-stu-id="77684-118">Example 3: Use an object reference to remove an SSL binding</span></span>
```
PS C:\>$WebApp = Get-AzureRmWebApp -Name "ContosoWebApp"
PS C:\> Remove-AzureRmWebAppSSLBinding -WebApp $WebApp -Name "www.contoso.com"
```

<span data-ttu-id="77684-119">這個範例使用 Web App 網站的物件參考來移除 Web 應用程式的 SSL 系結。</span><span class="sxs-lookup"><span data-stu-id="77684-119">This example uses an object reference to the Web App website to remove the SSL binding for a Web App.</span></span>

<span data-ttu-id="77684-120">第一個命令使用 Get-AzureRmWebApp Cmdlet 來建立名為 ContosoWebApp 的 Web App 的物件參考。</span><span class="sxs-lookup"><span data-stu-id="77684-120">The first command uses the Get-AzureRmWebApp cmdlet to create an object reference to the Web App named ContosoWebApp.</span></span>
<span data-ttu-id="77684-121">該物件參照會儲存在名為 $WebApp 的變數中。</span><span class="sxs-lookup"><span data-stu-id="77684-121">That object reference is stored in a variable named $WebApp.</span></span>

<span data-ttu-id="77684-122">第二個命令使用物件參照和 **AzureRmWebAppSSLBinding** Cmdlet 來移除 SSL 系結。</span><span class="sxs-lookup"><span data-stu-id="77684-122">The second command uses the object reference and the **Remove-AzureRmWebAppSSLBinding** cmdlet to remove the SSL binding.</span></span>

## <span data-ttu-id="77684-123">參數</span><span class="sxs-lookup"><span data-stu-id="77684-123">PARAMETERS</span></span>

### <span data-ttu-id="77684-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77684-124">-DefaultProfile</span></span>
<span data-ttu-id="77684-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="77684-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77684-126">-DeleteCertificate</span><span class="sxs-lookup"><span data-stu-id="77684-126">-DeleteCertificate</span></span>
<span data-ttu-id="77684-127">指定在移除 SSL 系結是憑證所使用的唯一系結時要發生的動作。</span><span class="sxs-lookup"><span data-stu-id="77684-127">Specifies the action to take place if the SSL binding being removed is the only binding used by the certificate.</span></span>
<span data-ttu-id="77684-128">如果 *DeleteCertificate* 設定為 $False，則刪除系結時，不會刪除憑證。</span><span class="sxs-lookup"><span data-stu-id="77684-128">If *DeleteCertificate* is set to $False, the certificate will not be deleted when the binding is deleted.</span></span>
<span data-ttu-id="77684-129">如果 *DeleteCertificate* 設定為 $True 或不包含在命令中，則會將憑證與 SSL 系結一起刪除。</span><span class="sxs-lookup"><span data-stu-id="77684-129">If *DeleteCertificate* is set to $True or is not included in the command, the certificate will be deleted along with the SSL binding.</span></span>

<span data-ttu-id="77684-130">只有在已移除 SSL 系結是認證所使用的唯一系結時，才能刪除證書。</span><span class="sxs-lookup"><span data-stu-id="77684-130">The certificate will only be deleted if the SSL binding being removed is the only binding used by the certificate.</span></span>
<span data-ttu-id="77684-131">如果憑證有一個以上的系結，不論 *DeleteCertificate* 參數的值為何，都不會移除證書。</span><span class="sxs-lookup"><span data-stu-id="77684-131">If the certificate has more than one binding, the certificate will not be removed regardless of the value of the *DeleteCertificate* parameter.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77684-132">-Force</span><span class="sxs-lookup"><span data-stu-id="77684-132">-Force</span></span>
<span data-ttu-id="77684-133">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="77684-133">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77684-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="77684-134">-Name</span></span>
<span data-ttu-id="77684-135">指定 Web 應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="77684-135">Specifies the name of the Web App.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77684-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77684-136">-ResourceGroupName</span></span>
<span data-ttu-id="77684-137">指定指派憑證的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="77684-137">Specifies the name of the resource group that the certificate is assigned to.</span></span>

<span data-ttu-id="77684-138">您無法在同一命令中使用 *ResourceGroupName* 參數和 *WebApp* 參數。</span><span class="sxs-lookup"><span data-stu-id="77684-138">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77684-139">-槽</span><span class="sxs-lookup"><span data-stu-id="77684-139">-Slot</span></span>
<span data-ttu-id="77684-140">指定 Web 應用程式部署槽。</span><span class="sxs-lookup"><span data-stu-id="77684-140">Specifies the Web App deployment slot.</span></span>
<span data-ttu-id="77684-141">若要取得部署槽，請使用 Get-AzureRMWebAppSlot Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="77684-141">To get a deployment slot, use the Get-AzureRMWebAppSlot cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77684-142">-WebApp</span><span class="sxs-lookup"><span data-stu-id="77684-142">-WebApp</span></span>
<span data-ttu-id="77684-143">指定 Web 應用程式。</span><span class="sxs-lookup"><span data-stu-id="77684-143">Specifies a Web App.</span></span>
<span data-ttu-id="77684-144">若要取得 Web 應用程式，請使用 Get-AzureRmWebApp Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="77684-144">To get a Web App, use the Get-AzureRmWebApp cmdlet.</span></span>

<span data-ttu-id="77684-145">您無法在與 *ResourceGroupName* 參數和/或 *WebAppName* 相同的命令中使用 *WebApp* 參數。</span><span class="sxs-lookup"><span data-stu-id="77684-145">You cannot use the *WebApp* parameter in the same command as the *ResourceGroupName* parameter and/or the *WebAppName*.</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="77684-146">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="77684-146">-WebAppName</span></span>
<span data-ttu-id="77684-147">指定 Web 應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="77684-147">Specifies the name of the Web App.</span></span>

<span data-ttu-id="77684-148">您無法在同一命令中使用 *WebAppName* 參數和 *WebApp* 參數。</span><span class="sxs-lookup"><span data-stu-id="77684-148">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77684-149">-確認</span><span class="sxs-lookup"><span data-stu-id="77684-149">-Confirm</span></span>
<span data-ttu-id="77684-150">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="77684-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77684-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77684-151">-WhatIf</span></span>
<span data-ttu-id="77684-152">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="77684-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77684-153">未執行 Cmdlet。顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="77684-153">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77684-154">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="77684-154">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77684-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77684-155">CommonParameters</span></span>
<span data-ttu-id="77684-156">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="77684-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77684-157">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="77684-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77684-158">輸入</span><span class="sxs-lookup"><span data-stu-id="77684-158">INPUTS</span></span>

### <span data-ttu-id="77684-159">網站地圖</span><span class="sxs-lookup"><span data-stu-id="77684-159">Site</span></span>
<span data-ttu-id="77684-160">形參 "WebApp" 接受管線中 "Site" 類型的值</span><span class="sxs-lookup"><span data-stu-id="77684-160">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="77684-161">輸出</span><span class="sxs-lookup"><span data-stu-id="77684-161">OUTPUTS</span></span>

## <span data-ttu-id="77684-162">筆記</span><span class="sxs-lookup"><span data-stu-id="77684-162">NOTES</span></span>

## <span data-ttu-id="77684-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="77684-163">RELATED LINKS</span></span>

[<span data-ttu-id="77684-164">AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="77684-164">Get-AzureRmWebAppSSLBinding</span></span>](./Get-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="77684-165">新-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="77684-165">New-AzureRmWebAppSSLBinding</span></span>](./New-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="77684-166">AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="77684-166">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="77684-167">AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="77684-167">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)


