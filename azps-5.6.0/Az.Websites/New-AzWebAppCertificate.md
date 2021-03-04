---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/new-AzWebAppCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppCertificate.md
ms.openlocfilehash: 8e4ed309d4109ecfe230a522a65054213ae32049
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907006"
---
# <span data-ttu-id="6f770-101">New-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="6f770-101">New-AzWebAppCertificate</span></span>

## <span data-ttu-id="6f770-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6f770-102">SYNOPSIS</span></span>
<span data-ttu-id="6f770-103">為 Azure Web App 建立 App 服務受管理的憑證。</span><span class="sxs-lookup"><span data-stu-id="6f770-103">Creates an App service managed certificate for an Azure Web App.</span></span> 

## <span data-ttu-id="6f770-104">語法</span><span class="sxs-lookup"><span data-stu-id="6f770-104">SYNTAX</span></span>

```
New-AzWebAppCertificate [-ResourceGroupName] <String> [-WebAppName] <String> [-Name] <String> [[-Slot] <String>]
 [-HostName] <String> [-AddBinding] [[-SslState] <SslState>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6f770-105">描述</span><span class="sxs-lookup"><span data-stu-id="6f770-105">DESCRIPTION</span></span>
<span data-ttu-id="6f770-106">**New-AzWebAppCertificate** Cmdlet 會建立 Azure 應用程式服務受管理憑證</span><span class="sxs-lookup"><span data-stu-id="6f770-106">The **New-AzWebAppCertificate** cmdlet creates an Azure App Service Managed Certificate</span></span>
## <span data-ttu-id="6f770-107">例子</span><span class="sxs-lookup"><span data-stu-id="6f770-107">EXAMPLES</span></span>

### <span data-ttu-id="6f770-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="6f770-108">Example 1</span></span>
```powershell
PS C:\> New-AzWebAppCertificate -ResourceGroupName Default-Web-WestUS -WebAppName "ContosoSite" -Name"ContosoCert" -HostName "www.ContosoSite.net"
```

<span data-ttu-id="6f770-109">此命令會為給定 WebApp 建立 App 服務受管理的憑證</span><span class="sxs-lookup"><span data-stu-id="6f770-109">This command create an App Service Managed Certificate for the given WebApp</span></span>

### <span data-ttu-id="6f770-110">範例 2</span><span class="sxs-lookup"><span data-stu-id="6f770-110">Example 2</span></span>
```powershell
PS C:\> New-AzWebAppCertificate -ResourceGroupName Default-Web-WestUS -WebAppName "ContosoSite" -Name"ContosoCert" -HostName "www.ContosoSite.net" -Slot "test" -AddCertBinding
```

<span data-ttu-id="6f770-111">此命令會建立 App 服務受管理的憑證，並綁定至給定 WebApp Slot。</span><span class="sxs-lookup"><span data-stu-id="6f770-111">This command create an App Service Managed Certificate and binds to the given WebApp Slot.</span></span>

### <span data-ttu-id="6f770-112">範例 3</span><span class="sxs-lookup"><span data-stu-id="6f770-112">Example 3</span></span>
```powershell
PS C:\> New-AzWebAppCertificate -ResourceGroupName Default-Web-WestUS -WebAppName "ContosoSite" -Name"ContosoCert" -HostName "www.ContosoSite.net" -AddBinding
```

<span data-ttu-id="6f770-113">此命令會建立 App 服務受管理的憑證，並綁定至給定 WebApp。</span><span class="sxs-lookup"><span data-stu-id="6f770-113">This command create an App Service Managed Certificate and binds to the given WebApp.</span></span>

## <span data-ttu-id="6f770-114">參數</span><span class="sxs-lookup"><span data-stu-id="6f770-114">PARAMETERS</span></span>

### <span data-ttu-id="6f770-115">-AddBinding</span><span class="sxs-lookup"><span data-stu-id="6f770-115">-AddBinding</span></span>
<span data-ttu-id="6f770-116">若要將建立憑證新增到 WebApp/slot。</span><span class="sxs-lookup"><span data-stu-id="6f770-116">To add the created certificate to WebApp/slot.</span></span>

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

### <span data-ttu-id="6f770-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f770-117">-DefaultProfile</span></span>
<span data-ttu-id="6f770-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6f770-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f770-119">-HostName</span><span class="sxs-lookup"><span data-stu-id="6f770-119">-HostName</span></span>
<span data-ttu-id="6f770-120">與 Web App/slot 相關聯的自訂主機名稱。</span><span class="sxs-lookup"><span data-stu-id="6f770-120">Custom hostnames associated with web app/slot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f770-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="6f770-121">-Name</span></span>
<span data-ttu-id="6f770-122">憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="6f770-122">The name of the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f770-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f770-123">-ResourceGroupName</span></span>
<span data-ttu-id="6f770-124">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6f770-124">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f770-125">-Slot</span><span class="sxs-lookup"><span data-stu-id="6f770-125">-Slot</span></span>
<span data-ttu-id="6f770-126">Web App 插槽的名稱。</span><span class="sxs-lookup"><span data-stu-id="6f770-126">The name of the web app slot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f770-127">-SslState</span><span class="sxs-lookup"><span data-stu-id="6f770-127">-SslState</span></span>
<span data-ttu-id="6f770-128">Ssl 狀態選項。</span><span class="sxs-lookup"><span data-stu-id="6f770-128">Ssl state option.</span></span>
<span data-ttu-id="6f770-129">使用 'SniEnabled' 或 'IpBasedEnabled'。</span><span class="sxs-lookup"><span data-stu-id="6f770-129">Use either 'SniEnabled' or 'IpBasedEnabled'.</span></span>
<span data-ttu-id="6f770-130">預設選項為 'SniEnabled'。</span><span class="sxs-lookup"><span data-stu-id="6f770-130">Default option is 'SniEnabled'.</span></span>

```yaml
Type: SslState
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, SniEnabled, IpBasedEnabled

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f770-131">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="6f770-131">-WebAppName</span></span>
<span data-ttu-id="6f770-132">Web 應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="6f770-132">The name of the web app.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f770-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f770-133">CommonParameters</span></span>
<span data-ttu-id="6f770-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6f770-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f770-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6f770-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f770-136">輸入</span><span class="sxs-lookup"><span data-stu-id="6f770-136">INPUTS</span></span>

### <span data-ttu-id="6f770-137">沒有</span><span class="sxs-lookup"><span data-stu-id="6f770-137">None</span></span>

## <span data-ttu-id="6f770-138">輸出</span><span class="sxs-lookup"><span data-stu-id="6f770-138">OUTPUTS</span></span>

### <span data-ttu-id="6f770-139">Microsoft.Azure.Commands.WebApps.models.WebApp.PSCertificate</span><span class="sxs-lookup"><span data-stu-id="6f770-139">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate</span></span>

## <span data-ttu-id="6f770-140">筆記</span><span class="sxs-lookup"><span data-stu-id="6f770-140">NOTES</span></span>

## <span data-ttu-id="6f770-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="6f770-141">RELATED LINKS</span></span>
[<span data-ttu-id="6f770-142">Remove-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="6f770-142">Remove-AzWebAppCertificate</span></span>](./Remove-AzWebAppCertificate.md)