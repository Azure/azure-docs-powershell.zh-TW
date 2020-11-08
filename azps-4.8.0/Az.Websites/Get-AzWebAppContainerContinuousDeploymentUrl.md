---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappcontainercontinuousdeploymenturl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppContainerContinuousDeploymentUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppContainerContinuousDeploymentUrl.md
ms.openlocfilehash: 2b49b30c06f39561f6d00542dd4ff02df56ee569
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128399"
---
# <span data-ttu-id="75d2c-101">Get-AzWebAppContainerContinuousDeploymentUrl</span><span class="sxs-lookup"><span data-stu-id="75d2c-101">Get-AzWebAppContainerContinuousDeploymentUrl</span></span>

## <span data-ttu-id="75d2c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="75d2c-102">SYNOPSIS</span></span>
<span data-ttu-id="75d2c-103">Get-AzWebAppContainerContinuousDeploymentUrl 將會傳回容器連續部署 url</span><span class="sxs-lookup"><span data-stu-id="75d2c-103">Get-AzWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

## <span data-ttu-id="75d2c-104">句法</span><span class="sxs-lookup"><span data-stu-id="75d2c-104">SYNTAX</span></span>

### <span data-ttu-id="75d2c-105">S1 (預設) </span><span class="sxs-lookup"><span data-stu-id="75d2c-105">S1 (Default)</span></span>
```
Get-AzWebAppContainerContinuousDeploymentUrl [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75d2c-106">S2</span><span class="sxs-lookup"><span data-stu-id="75d2c-106">S2</span></span>
```
Get-AzWebAppContainerContinuousDeploymentUrl [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="75d2c-107">說明</span><span class="sxs-lookup"><span data-stu-id="75d2c-107">DESCRIPTION</span></span>
<span data-ttu-id="75d2c-108">Get-AzWebAppContainerContinuousDeploymentUrl 將會傳回容器連續部署 url</span><span class="sxs-lookup"><span data-stu-id="75d2c-108">Get-AzWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

## <span data-ttu-id="75d2c-109">示例</span><span class="sxs-lookup"><span data-stu-id="75d2c-109">EXAMPLES</span></span>

### <span data-ttu-id="75d2c-110">範例1</span><span class="sxs-lookup"><span data-stu-id="75d2c-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppContainerContinuousDeploymentUrl -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="75d2c-111">這個命令會傳回容器連續部署 url。</span><span class="sxs-lookup"><span data-stu-id="75d2c-111">This command will return container continuous deployment url.</span></span>

## <span data-ttu-id="75d2c-112">參數</span><span class="sxs-lookup"><span data-stu-id="75d2c-112">PARAMETERS</span></span>

### <span data-ttu-id="75d2c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75d2c-113">-DefaultProfile</span></span>
<span data-ttu-id="75d2c-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="75d2c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75d2c-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="75d2c-115">-Name</span></span>
<span data-ttu-id="75d2c-116">Web 應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="75d2c-116">The name of the web app.</span></span>

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

### <span data-ttu-id="75d2c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75d2c-117">-ResourceGroupName</span></span>
<span data-ttu-id="75d2c-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="75d2c-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="75d2c-119">-SlotName</span><span class="sxs-lookup"><span data-stu-id="75d2c-119">-SlotName</span></span>
<span data-ttu-id="75d2c-120">Web 應用程式槽的名稱。</span><span class="sxs-lookup"><span data-stu-id="75d2c-120">The name of the web app slot.</span></span>

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

### <span data-ttu-id="75d2c-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="75d2c-121">-WebApp</span></span>
<span data-ttu-id="75d2c-122">Web app 物件</span><span class="sxs-lookup"><span data-stu-id="75d2c-122">The web app object</span></span>

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

### <span data-ttu-id="75d2c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75d2c-123">CommonParameters</span></span>
<span data-ttu-id="75d2c-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="75d2c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75d2c-125">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="75d2c-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75d2c-126">輸入</span><span class="sxs-lookup"><span data-stu-id="75d2c-126">INPUTS</span></span>

### <span data-ttu-id="75d2c-127">System.object</span><span class="sxs-lookup"><span data-stu-id="75d2c-127">System.String</span></span>

### <span data-ttu-id="75d2c-128">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="75d2c-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="75d2c-129">輸出</span><span class="sxs-lookup"><span data-stu-id="75d2c-129">OUTPUTS</span></span>

### <span data-ttu-id="75d2c-130">System.object</span><span class="sxs-lookup"><span data-stu-id="75d2c-130">System.String</span></span>

## <span data-ttu-id="75d2c-131">筆記</span><span class="sxs-lookup"><span data-stu-id="75d2c-131">NOTES</span></span>

## <span data-ttu-id="75d2c-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="75d2c-132">RELATED LINKS</span></span>
