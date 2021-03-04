---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azwebappcontainercontinuousdeploymenturl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppContainerContinuousDeploymentUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppContainerContinuousDeploymentUrl.md
ms.openlocfilehash: 90aca2939721144500519329492e04786b67a93a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909361"
---
# <span data-ttu-id="91d54-101">Get-AzWebAppContainerContinuousDeploymentUrl</span><span class="sxs-lookup"><span data-stu-id="91d54-101">Get-AzWebAppContainerContinuousDeploymentUrl</span></span>

## <span data-ttu-id="91d54-102">簡介</span><span class="sxs-lookup"><span data-stu-id="91d54-102">SYNOPSIS</span></span>
<span data-ttu-id="91d54-103">Get-AzWebAppContainerContinuousDeploymentUrl容器連續部署 URL</span><span class="sxs-lookup"><span data-stu-id="91d54-103">Get-AzWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

## <span data-ttu-id="91d54-104">語法</span><span class="sxs-lookup"><span data-stu-id="91d54-104">SYNTAX</span></span>

### <span data-ttu-id="91d54-105">S1 (預設) </span><span class="sxs-lookup"><span data-stu-id="91d54-105">S1 (Default)</span></span>
```
Get-AzWebAppContainerContinuousDeploymentUrl [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91d54-106">S2</span><span class="sxs-lookup"><span data-stu-id="91d54-106">S2</span></span>
```
Get-AzWebAppContainerContinuousDeploymentUrl [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="91d54-107">描述</span><span class="sxs-lookup"><span data-stu-id="91d54-107">DESCRIPTION</span></span>
<span data-ttu-id="91d54-108">Get-AzWebAppContainerContinuousDeploymentUrl容器連續部署 URL</span><span class="sxs-lookup"><span data-stu-id="91d54-108">Get-AzWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

## <span data-ttu-id="91d54-109">例子</span><span class="sxs-lookup"><span data-stu-id="91d54-109">EXAMPLES</span></span>

### <span data-ttu-id="91d54-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="91d54-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppContainerContinuousDeploymentUrl -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="91d54-111">此命令會返回容器連續部署 URL。</span><span class="sxs-lookup"><span data-stu-id="91d54-111">This command will return container continuous deployment url.</span></span>

## <span data-ttu-id="91d54-112">參數</span><span class="sxs-lookup"><span data-stu-id="91d54-112">PARAMETERS</span></span>

### <span data-ttu-id="91d54-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91d54-113">-DefaultProfile</span></span>
<span data-ttu-id="91d54-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="91d54-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91d54-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="91d54-115">-Name</span></span>
<span data-ttu-id="91d54-116">Web 應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="91d54-116">The name of the web app.</span></span>

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

### <span data-ttu-id="91d54-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91d54-117">-ResourceGroupName</span></span>
<span data-ttu-id="91d54-118">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="91d54-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="91d54-119">-SlotName</span><span class="sxs-lookup"><span data-stu-id="91d54-119">-SlotName</span></span>
<span data-ttu-id="91d54-120">Web App 插槽的名稱。</span><span class="sxs-lookup"><span data-stu-id="91d54-120">The name of the web app slot.</span></span>

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

### <span data-ttu-id="91d54-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="91d54-121">-WebApp</span></span>
<span data-ttu-id="91d54-122">Web App 物件</span><span class="sxs-lookup"><span data-stu-id="91d54-122">The web app object</span></span>

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

### <span data-ttu-id="91d54-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91d54-123">CommonParameters</span></span>
<span data-ttu-id="91d54-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="91d54-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91d54-125">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="91d54-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91d54-126">輸入</span><span class="sxs-lookup"><span data-stu-id="91d54-126">INPUTS</span></span>

### <span data-ttu-id="91d54-127">System.String</span><span class="sxs-lookup"><span data-stu-id="91d54-127">System.String</span></span>

### <span data-ttu-id="91d54-128">Microsoft.Azure.Commands.WebApps.models.PSSite</span><span class="sxs-lookup"><span data-stu-id="91d54-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="91d54-129">輸出</span><span class="sxs-lookup"><span data-stu-id="91d54-129">OUTPUTS</span></span>

### <span data-ttu-id="91d54-130">System.String</span><span class="sxs-lookup"><span data-stu-id="91d54-130">System.String</span></span>

## <span data-ttu-id="91d54-131">筆記</span><span class="sxs-lookup"><span data-stu-id="91d54-131">NOTES</span></span>

## <span data-ttu-id="91d54-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="91d54-132">RELATED LINKS</span></span>
