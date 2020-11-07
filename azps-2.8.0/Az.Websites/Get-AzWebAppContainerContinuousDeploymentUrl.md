---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappcontainercontinuousdeploymenturl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppContainerContinuousDeploymentUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppContainerContinuousDeploymentUrl.md
ms.openlocfilehash: ed7ad2edb0c82203f571edccf9b6672428956ac2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93793281"
---
# <span data-ttu-id="f6a91-101">Get-AzWebAppContainerContinuousDeploymentUrl</span><span class="sxs-lookup"><span data-stu-id="f6a91-101">Get-AzWebAppContainerContinuousDeploymentUrl</span></span>

## <span data-ttu-id="f6a91-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f6a91-102">SYNOPSIS</span></span>
<span data-ttu-id="f6a91-103">Get-AzWebAppContainerContinuousDeploymentUrl 將會傳回容器連續部署 url</span><span class="sxs-lookup"><span data-stu-id="f6a91-103">Get-AzWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

## <span data-ttu-id="f6a91-104">句法</span><span class="sxs-lookup"><span data-stu-id="f6a91-104">SYNTAX</span></span>

### <span data-ttu-id="f6a91-105">S1 (預設) </span><span class="sxs-lookup"><span data-stu-id="f6a91-105">S1 (Default)</span></span>
```
Get-AzWebAppContainerContinuousDeploymentUrl [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6a91-106">S2</span><span class="sxs-lookup"><span data-stu-id="f6a91-106">S2</span></span>
```
Get-AzWebAppContainerContinuousDeploymentUrl [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f6a91-107">說明</span><span class="sxs-lookup"><span data-stu-id="f6a91-107">DESCRIPTION</span></span>
<span data-ttu-id="f6a91-108">Get-AzWebAppContainerContinuousDeploymentUrl 將會傳回容器連續部署 url</span><span class="sxs-lookup"><span data-stu-id="f6a91-108">Get-AzWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

## <span data-ttu-id="f6a91-109">示例</span><span class="sxs-lookup"><span data-stu-id="f6a91-109">EXAMPLES</span></span>

### <span data-ttu-id="f6a91-110">範例1</span><span class="sxs-lookup"><span data-stu-id="f6a91-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppContainerContinuousDeploymentUrl -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="f6a91-111">這個命令會傳回容器連續部署 url。</span><span class="sxs-lookup"><span data-stu-id="f6a91-111">This command will return container continuous deployment url.</span></span>

## <span data-ttu-id="f6a91-112">參數</span><span class="sxs-lookup"><span data-stu-id="f6a91-112">PARAMETERS</span></span>

### <span data-ttu-id="f6a91-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6a91-113">-DefaultProfile</span></span>
<span data-ttu-id="f6a91-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f6a91-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6a91-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="f6a91-115">-Name</span></span>
<span data-ttu-id="f6a91-116">Web 應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="f6a91-116">The name of the web app.</span></span>

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

### <span data-ttu-id="f6a91-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6a91-117">-ResourceGroupName</span></span>
<span data-ttu-id="f6a91-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f6a91-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="f6a91-119">-SlotName</span><span class="sxs-lookup"><span data-stu-id="f6a91-119">-SlotName</span></span>
<span data-ttu-id="f6a91-120">Web 應用程式槽的名稱。</span><span class="sxs-lookup"><span data-stu-id="f6a91-120">The name of the web app slot.</span></span>

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

### <span data-ttu-id="f6a91-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="f6a91-121">-WebApp</span></span>
<span data-ttu-id="f6a91-122">Web app 物件</span><span class="sxs-lookup"><span data-stu-id="f6a91-122">The web app object</span></span>

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

### <span data-ttu-id="f6a91-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6a91-123">CommonParameters</span></span>
<span data-ttu-id="f6a91-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f6a91-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6a91-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f6a91-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6a91-126">輸入</span><span class="sxs-lookup"><span data-stu-id="f6a91-126">INPUTS</span></span>

### <span data-ttu-id="f6a91-127">System.object</span><span class="sxs-lookup"><span data-stu-id="f6a91-127">System.String</span></span>

### <span data-ttu-id="f6a91-128">PSSite 中的 WebApps。</span><span class="sxs-lookup"><span data-stu-id="f6a91-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="f6a91-129">輸出</span><span class="sxs-lookup"><span data-stu-id="f6a91-129">OUTPUTS</span></span>

### <span data-ttu-id="f6a91-130">System.object</span><span class="sxs-lookup"><span data-stu-id="f6a91-130">System.String</span></span>

## <span data-ttu-id="f6a91-131">筆記</span><span class="sxs-lookup"><span data-stu-id="f6a91-131">NOTES</span></span>

## <span data-ttu-id="f6a91-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="f6a91-132">RELATED LINKS</span></span>
