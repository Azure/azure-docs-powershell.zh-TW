---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-AzWebAppCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppCertificate.md
ms.openlocfilehash: 56f8d69325e5a7918668ac2807449f348e73c91b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100130239"
---
# <span data-ttu-id="695d8-101">New-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="695d8-101">New-AzWebAppCertificate</span></span>

## <span data-ttu-id="695d8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="695d8-102">SYNOPSIS</span></span>
<span data-ttu-id="695d8-103">針對 Azure Web App 建立應用程式服務管理的憑證。</span><span class="sxs-lookup"><span data-stu-id="695d8-103">Creates an App service managed certificate for an Azure Web App.</span></span> 

## <span data-ttu-id="695d8-104">句法</span><span class="sxs-lookup"><span data-stu-id="695d8-104">SYNTAX</span></span>

```
New-AzWebAppCertificate [-ResourceGroupName] <String> [-WebAppName] <String> [-Name] <String> [[-Slot] <String>]
 [-HostName] <String> [-AddBinding] [[-SslState] <SslState>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="695d8-105">說明</span><span class="sxs-lookup"><span data-stu-id="695d8-105">DESCRIPTION</span></span>
<span data-ttu-id="695d8-106">**新的-AzWebAppCertificate** Cmdlet 會建立 Azure App 服務管理的憑證</span><span class="sxs-lookup"><span data-stu-id="695d8-106">The **New-AzWebAppCertificate** cmdlet creates an Azure App Service Managed Certificate</span></span>
## <span data-ttu-id="695d8-107">示例</span><span class="sxs-lookup"><span data-stu-id="695d8-107">EXAMPLES</span></span>

### <span data-ttu-id="695d8-108">範例1</span><span class="sxs-lookup"><span data-stu-id="695d8-108">Example 1</span></span>
```powershell
PS C:\> New-AzWebAppCertificate -ResourceGroupName Default-Web-WestUS -WebAppName "ContosoSite" -Name"ContosoCert" -HostName "www.ContosoSite.net"
```

<span data-ttu-id="695d8-109">這個命令會為指定的 WebApp 建立應用程式服務管理的憑證</span><span class="sxs-lookup"><span data-stu-id="695d8-109">This command create an App Service Managed Certificate for the given WebApp</span></span>

### <span data-ttu-id="695d8-110">範例2</span><span class="sxs-lookup"><span data-stu-id="695d8-110">Example 2</span></span>
```powershell
PS C:\> New-AzWebAppCertificate -ResourceGroupName Default-Web-WestUS -WebAppName "ContosoSite" -Name"ContosoCert" -HostName "www.ContosoSite.net" -Slot "test" -AddCertBinding
```

<span data-ttu-id="695d8-111">這個命令會建立應用程式服務管理的憑證，並系結到指定的 WebApp 槽。</span><span class="sxs-lookup"><span data-stu-id="695d8-111">This command create an App Service Managed Certificate and binds to the given WebApp Slot.</span></span>

### <span data-ttu-id="695d8-112">範例3</span><span class="sxs-lookup"><span data-stu-id="695d8-112">Example 3</span></span>
```powershell
PS C:\> New-AzWebAppCertificate -ResourceGroupName Default-Web-WestUS -WebAppName "ContosoSite" -Name"ContosoCert" -HostName "www.ContosoSite.net" -AddBinding
```

<span data-ttu-id="695d8-113">這個命令會建立應用程式服務管理的憑證，並系結到指定的 WebApp。</span><span class="sxs-lookup"><span data-stu-id="695d8-113">This command create an App Service Managed Certificate and binds to the given WebApp.</span></span>

## <span data-ttu-id="695d8-114">參數</span><span class="sxs-lookup"><span data-stu-id="695d8-114">PARAMETERS</span></span>

### <span data-ttu-id="695d8-115">-AddBinding</span><span class="sxs-lookup"><span data-stu-id="695d8-115">-AddBinding</span></span>
<span data-ttu-id="695d8-116">將已建立的憑證新增至 WebApp/槽位。</span><span class="sxs-lookup"><span data-stu-id="695d8-116">To add the created certificate to WebApp/slot.</span></span>

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

### <span data-ttu-id="695d8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="695d8-117">-DefaultProfile</span></span>
<span data-ttu-id="695d8-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="695d8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="695d8-119">-HostName</span><span class="sxs-lookup"><span data-stu-id="695d8-119">-HostName</span></span>
<span data-ttu-id="695d8-120">與 web 應用程式/槽關聯的自訂主機名稱。</span><span class="sxs-lookup"><span data-stu-id="695d8-120">Custom hostnames associated with web app/slot.</span></span>

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

### <span data-ttu-id="695d8-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="695d8-121">-Name</span></span>
<span data-ttu-id="695d8-122">憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="695d8-122">The name of the certificate.</span></span>

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

### <span data-ttu-id="695d8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="695d8-123">-ResourceGroupName</span></span>
<span data-ttu-id="695d8-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="695d8-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="695d8-125">-槽</span><span class="sxs-lookup"><span data-stu-id="695d8-125">-Slot</span></span>
<span data-ttu-id="695d8-126">Web 應用程式槽的名稱。</span><span class="sxs-lookup"><span data-stu-id="695d8-126">The name of the web app slot.</span></span>

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

### <span data-ttu-id="695d8-127">-SslState</span><span class="sxs-lookup"><span data-stu-id="695d8-127">-SslState</span></span>
<span data-ttu-id="695d8-128">[Ssl 狀態] 選項。</span><span class="sxs-lookup"><span data-stu-id="695d8-128">Ssl state option.</span></span>
<span data-ttu-id="695d8-129">使用 "SniEnabled" 或 "IpBasedEnabled"。</span><span class="sxs-lookup"><span data-stu-id="695d8-129">Use either 'SniEnabled' or 'IpBasedEnabled'.</span></span>
<span data-ttu-id="695d8-130">預設選項為 [SniEnabled]。</span><span class="sxs-lookup"><span data-stu-id="695d8-130">Default option is 'SniEnabled'.</span></span>

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

### <span data-ttu-id="695d8-131">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="695d8-131">-WebAppName</span></span>
<span data-ttu-id="695d8-132">Web 應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="695d8-132">The name of the web app.</span></span>

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

### <span data-ttu-id="695d8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="695d8-133">CommonParameters</span></span>
<span data-ttu-id="695d8-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="695d8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="695d8-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="695d8-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="695d8-136">輸入</span><span class="sxs-lookup"><span data-stu-id="695d8-136">INPUTS</span></span>

### <span data-ttu-id="695d8-137">所有</span><span class="sxs-lookup"><span data-stu-id="695d8-137">None</span></span>

## <span data-ttu-id="695d8-138">輸出</span><span class="sxs-lookup"><span data-stu-id="695d8-138">OUTPUTS</span></span>

### <span data-ttu-id="695d8-139">WebApps WebApp. PSCertificate （）</span><span class="sxs-lookup"><span data-stu-id="695d8-139">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate</span></span>

## <span data-ttu-id="695d8-140">筆記</span><span class="sxs-lookup"><span data-stu-id="695d8-140">NOTES</span></span>

## <span data-ttu-id="695d8-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="695d8-141">RELATED LINKS</span></span>
[<span data-ttu-id="695d8-142">移除-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="695d8-142">Remove-AzWebAppCertificate</span></span>](./Remove-AzWebAppCertificate.md)