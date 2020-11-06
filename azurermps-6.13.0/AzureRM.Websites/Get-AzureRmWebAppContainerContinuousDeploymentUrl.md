---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/?view=azurermps-6.8.1
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppContainerContinuousDeploymentUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppContainerContinuousDeploymentUrl.md
ms.openlocfilehash: 0618b7c4cc4f9ee8b2342306e4aadf83ff0c17f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448866"
---
# <span data-ttu-id="cf7ea-101">Get-AzureRmWebAppContainerContinuousDeploymentUrl</span><span class="sxs-lookup"><span data-stu-id="cf7ea-101">Get-AzureRmWebAppContainerContinuousDeploymentUrl</span></span>

## <span data-ttu-id="cf7ea-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cf7ea-102">SYNOPSIS</span></span>
<span data-ttu-id="cf7ea-103">Get-AzureRMWebAppContainerContinuousDeploymentUrl 將會傳回容器連續部署 url</span><span class="sxs-lookup"><span data-stu-id="cf7ea-103">Get-AzureRMWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf7ea-104">句法</span><span class="sxs-lookup"><span data-stu-id="cf7ea-104">SYNTAX</span></span>

### <span data-ttu-id="cf7ea-105">S1</span><span class="sxs-lookup"><span data-stu-id="cf7ea-105">S1</span></span>
```
Get-AzureRmWebAppContainerContinuousDeploymentUrl [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf7ea-106">S2</span><span class="sxs-lookup"><span data-stu-id="cf7ea-106">S2</span></span>
```
Get-AzureRmWebAppContainerContinuousDeploymentUrl [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cf7ea-107">說明</span><span class="sxs-lookup"><span data-stu-id="cf7ea-107">DESCRIPTION</span></span>
<span data-ttu-id="cf7ea-108">Get-AzureRMWebAppContainerContinuousDeploymentUrl 將會傳回容器連續部署 url</span><span class="sxs-lookup"><span data-stu-id="cf7ea-108">Get-AzureRMWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

## <span data-ttu-id="cf7ea-109">示例</span><span class="sxs-lookup"><span data-stu-id="cf7ea-109">EXAMPLES</span></span>

### <span data-ttu-id="cf7ea-110">範例1</span><span class="sxs-lookup"><span data-stu-id="cf7ea-110">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppContainerContinuousDeploymentUrl -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="cf7ea-111">這個命令會傳回容器連續部署 url。</span><span class="sxs-lookup"><span data-stu-id="cf7ea-111">This command will return container continuous deployment url.</span></span>

## <span data-ttu-id="cf7ea-112">參數</span><span class="sxs-lookup"><span data-stu-id="cf7ea-112">PARAMETERS</span></span>

### <span data-ttu-id="cf7ea-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf7ea-113">-DefaultProfile</span></span>
<span data-ttu-id="cf7ea-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cf7ea-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf7ea-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="cf7ea-115">-Name</span></span>
<span data-ttu-id="cf7ea-116">Web 應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="cf7ea-116">The name of the web app.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf7ea-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf7ea-117">-ResourceGroupName</span></span>
<span data-ttu-id="cf7ea-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cf7ea-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="cf7ea-119">-SlotName</span><span class="sxs-lookup"><span data-stu-id="cf7ea-119">-SlotName</span></span>
<span data-ttu-id="cf7ea-120">Web 應用程式槽的名稱。</span><span class="sxs-lookup"><span data-stu-id="cf7ea-120">The name of the web app slot.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf7ea-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="cf7ea-121">-WebApp</span></span>
<span data-ttu-id="cf7ea-122">Web app 物件</span><span class="sxs-lookup"><span data-stu-id="cf7ea-122">The web app object</span></span>

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

### <span data-ttu-id="cf7ea-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf7ea-123">CommonParameters</span></span>
<span data-ttu-id="cf7ea-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cf7ea-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf7ea-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cf7ea-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf7ea-126">輸入</span><span class="sxs-lookup"><span data-stu-id="cf7ea-126">INPUTS</span></span>

### <span data-ttu-id="cf7ea-127">System.object</span><span class="sxs-lookup"><span data-stu-id="cf7ea-127">System.String</span></span>
### <span data-ttu-id="cf7ea-128">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="cf7ea-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>
## <span data-ttu-id="cf7ea-129">輸出</span><span class="sxs-lookup"><span data-stu-id="cf7ea-129">OUTPUTS</span></span>

### <span data-ttu-id="cf7ea-130">System.object</span><span class="sxs-lookup"><span data-stu-id="cf7ea-130">System.String</span></span>
## <span data-ttu-id="cf7ea-131">筆記</span><span class="sxs-lookup"><span data-stu-id="cf7ea-131">NOTES</span></span>

## <span data-ttu-id="cf7ea-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="cf7ea-132">RELATED LINKS</span></span>
