---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EE3D2BA0-32E7-4A37-BCAF-F0E8FAAC43CE
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
ms.openlocfilehash: 08a9fbd9798a3fd3b53d7d71aca9ebd607d23164
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907346"
---
# <span data-ttu-id="9a650-101">Get-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="9a650-101">Get-AzWebAppSSLBinding</span></span>

## <span data-ttu-id="9a650-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9a650-102">SYNOPSIS</span></span>
<span data-ttu-id="9a650-103">獲得 Azure Web App 憑證 SSL 綁定。</span><span class="sxs-lookup"><span data-stu-id="9a650-103">Gets an Azure Web App certificate SSL binding.</span></span>

## <span data-ttu-id="9a650-104">語法</span><span class="sxs-lookup"><span data-stu-id="9a650-104">SYNTAX</span></span>

### <span data-ttu-id="9a650-105">S1</span><span class="sxs-lookup"><span data-stu-id="9a650-105">S1</span></span>
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-ResourceGroupName] <String> [-WebAppName] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a650-106">S2</span><span class="sxs-lookup"><span data-stu-id="9a650-106">S2</span></span>
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9a650-107">描述</span><span class="sxs-lookup"><span data-stu-id="9a650-107">DESCRIPTION</span></span>
<span data-ttu-id="9a650-108">**Get-AzWebAppSSLBinding** Cmdlet 會為 Azure Web App (SSL) 安全通訊端層。</span><span class="sxs-lookup"><span data-stu-id="9a650-108">The **Get-AzWebAppSSLBinding** cmdlet gets a Secure Sockets Layer (SSL) binding for an Azure Web App.</span></span>
<span data-ttu-id="9a650-109">SSL 系帶可用來將 Web App 與上傳的憑證建立關聯。</span><span class="sxs-lookup"><span data-stu-id="9a650-109">SSL bindings are used to associate a Web App with an uploaded certificate.</span></span>
<span data-ttu-id="9a650-110">Web App 可以綁定至多個憑證。</span><span class="sxs-lookup"><span data-stu-id="9a650-110">Web Apps can be bound to multiple certificates.</span></span>

## <span data-ttu-id="9a650-111">例子</span><span class="sxs-lookup"><span data-stu-id="9a650-111">EXAMPLES</span></span>

### <span data-ttu-id="9a650-112">範例 1：取得 Web App 的 SSL 綁定</span><span class="sxs-lookup"><span data-stu-id="9a650-112">Example 1: Get SSL bindings for a Web App</span></span>
```
PS C:\>Get-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp"
```

<span data-ttu-id="9a650-113">此命令會針對與資源群組 ContosoResourceGroup 相關聯的 Web App ContosoWebApp，來取回 SSL 綁定。</span><span class="sxs-lookup"><span data-stu-id="9a650-113">This command retrieves the SSL bindings for the Web App ContosoWebApp, which is associated with the resource group ContosoResourceGroup.</span></span>

### <span data-ttu-id="9a650-114">範例 2：使用物件參照取得 Web App 的 SSL 綁定</span><span class="sxs-lookup"><span data-stu-id="9a650-114">Example 2: Use an object reference to get SSL bindings for a Web App</span></span>
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Get-AzWebAppSSLBinding -WebApp $WebApp
```

<span data-ttu-id="9a650-115">此範例中的命令也會取得 Web App ContosoWebApp 的 SSL 綁定;不過，在此案例中，會使用物件參照，而不是使用 Web App 名稱和相關聯的資源組名。</span><span class="sxs-lookup"><span data-stu-id="9a650-115">The commands in this example also get the SSL bindings for the Web App ContosoWebApp; in this case, however, an object reference is used instead of the Web App name and the name of the associated resource group.</span></span>
<span data-ttu-id="9a650-116">此物件參照是由範例中的第一個命令所建立，該命令使用 **Get-AzWebApp** 建立名為 ContosoWebApp 的 Web App 物件參照。</span><span class="sxs-lookup"><span data-stu-id="9a650-116">This object reference is created by the first command in the example, which uses **Get-AzWebApp** to create an object reference to the Web App named ContosoWebApp.</span></span>
<span data-ttu-id="9a650-117">該物件參照會儲存在名為 $WebApp 的變數中。</span><span class="sxs-lookup"><span data-stu-id="9a650-117">That object reference is stored in a variable named $WebApp.</span></span>
<span data-ttu-id="9a650-118">接著，第二個命令會使用 **這個變數和 Get-AzWebAppSSLBinding** Cmdlet 來取得 SSL 綁定。</span><span class="sxs-lookup"><span data-stu-id="9a650-118">This variable, and the **Get-AzWebAppSSLBinding** cmdlet, are then used by the second command to get the SSL bindings.</span></span>

## <span data-ttu-id="9a650-119">參數</span><span class="sxs-lookup"><span data-stu-id="9a650-119">PARAMETERS</span></span>

### <span data-ttu-id="9a650-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a650-120">-DefaultProfile</span></span>
<span data-ttu-id="9a650-121">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9a650-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a650-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="9a650-122">-Name</span></span>
<span data-ttu-id="9a650-123">指定 SSL 綁定的名稱。</span><span class="sxs-lookup"><span data-stu-id="9a650-123">Specifies the name of the SSL binding.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a650-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a650-124">-ResourceGroupName</span></span>
<span data-ttu-id="9a650-125">指定憑證指派給的資源組名。</span><span class="sxs-lookup"><span data-stu-id="9a650-125">Specifies the name of the resource group that the certificate is assigned to.</span></span>
<span data-ttu-id="9a650-126">您無法在同一 *個命令中使用 ResourceGroupName* 參數和 *WebApp* 參數。</span><span class="sxs-lookup"><span data-stu-id="9a650-126">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="9a650-127">-Slot</span><span class="sxs-lookup"><span data-stu-id="9a650-127">-Slot</span></span>
<span data-ttu-id="9a650-128">指定 Web App 部署時段。</span><span class="sxs-lookup"><span data-stu-id="9a650-128">Specifies a Web App deployment slot.</span></span>
<span data-ttu-id="9a650-129">若要取得部署插槽，請使用 Get-AzWebAppSlot Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9a650-129">To get a deployment slot, use the Get-AzWebAppSlot cmdlet.</span></span>

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

### <span data-ttu-id="9a650-130">-WebApp</span><span class="sxs-lookup"><span data-stu-id="9a650-130">-WebApp</span></span>
<span data-ttu-id="9a650-131">指定 Web App。</span><span class="sxs-lookup"><span data-stu-id="9a650-131">Specifies a Web App.</span></span>
<span data-ttu-id="9a650-132">若要取得 Web App，請使用 Get-AzWebApp Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9a650-132">To get a Web App, use the Get-AzWebApp cmdlet.</span></span>

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

### <span data-ttu-id="9a650-133">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="9a650-133">-WebAppName</span></span>
<span data-ttu-id="9a650-134">指定此 Cmdlet 可獲取 SSL 綁定的 Web App 名稱。</span><span class="sxs-lookup"><span data-stu-id="9a650-134">Specifies the name of the Web App that this cmdlet gets SSL bindings from.</span></span>
<span data-ttu-id="9a650-135">您無法在同一個命令中使用 *WebAppName* 參數和 *WebApp* 參數。</span><span class="sxs-lookup"><span data-stu-id="9a650-135">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="9a650-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a650-136">CommonParameters</span></span>
<span data-ttu-id="9a650-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9a650-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a650-138">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="9a650-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a650-139">輸入</span><span class="sxs-lookup"><span data-stu-id="9a650-139">INPUTS</span></span>

### <span data-ttu-id="9a650-140">Microsoft.Azure.Commands.WebApps.models.PSSite</span><span class="sxs-lookup"><span data-stu-id="9a650-140">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="9a650-141">輸出</span><span class="sxs-lookup"><span data-stu-id="9a650-141">OUTPUTS</span></span>

### <span data-ttu-id="9a650-142">Microsoft.Azure.management.Websites.models.HostNameSslState</span><span class="sxs-lookup"><span data-stu-id="9a650-142">Microsoft.Azure.Management.WebSites.Models.HostNameSslState</span></span>

## <span data-ttu-id="9a650-143">筆記</span><span class="sxs-lookup"><span data-stu-id="9a650-143">NOTES</span></span>

## <span data-ttu-id="9a650-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="9a650-144">RELATED LINKS</span></span>

[<span data-ttu-id="9a650-145">New-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="9a650-145">New-AzWebAppSSLBinding</span></span>](./New-AzWebAppSSLBinding.md)

[<span data-ttu-id="9a650-146">Remove-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="9a650-146">Remove-AzWebAppSSLBinding</span></span>](./Remove-AzWebAppSSLBinding.md)

[<span data-ttu-id="9a650-147">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="9a650-147">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


