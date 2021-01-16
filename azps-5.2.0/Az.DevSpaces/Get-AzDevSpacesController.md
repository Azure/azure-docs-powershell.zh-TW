---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/get-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Get-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Get-AzDevSpacesController.md
ms.openlocfilehash: 56b26c48316fbcf5c0000a6904c71a655962aae0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98274903"
---
# <span data-ttu-id="5db81-101">Get-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="5db81-101">Get-AzDevSpacesController</span></span>

## <span data-ttu-id="5db81-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5db81-102">SYNOPSIS</span></span>
<span data-ttu-id="5db81-103">取得或列出 Azure DevSpaces 控制器。</span><span class="sxs-lookup"><span data-stu-id="5db81-103">Get or list Azure DevSpaces controller.</span></span>

## <span data-ttu-id="5db81-104">句法</span><span class="sxs-lookup"><span data-stu-id="5db81-104">SYNTAX</span></span>

### <span data-ttu-id="5db81-105">ListDevSpacesControllerParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="5db81-105">ListDevSpacesControllerParameterSet (Default)</span></span>
```
Get-AzDevSpacesController [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5db81-106">DevSpacesControllerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5db81-106">DevSpacesControllerNameParameterSet</span></span>
```
Get-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5db81-107">說明</span><span class="sxs-lookup"><span data-stu-id="5db81-107">DESCRIPTION</span></span>
<span data-ttu-id="5db81-108">取得或列出 Azure DevSpaces 控制器。</span><span class="sxs-lookup"><span data-stu-id="5db81-108">Get or list Azure DevSpaces controller.</span></span>

## <span data-ttu-id="5db81-109">示例</span><span class="sxs-lookup"><span data-stu-id="5db81-109">EXAMPLES</span></span>

### <span data-ttu-id="5db81-110">範例1</span><span class="sxs-lookup"><span data-stu-id="5db81-110">Example 1</span></span>
```powershell
PS C:\> Get-AzDevSpacesController

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="5db81-111">列出訂閱中的所有控制器。</span><span class="sxs-lookup"><span data-stu-id="5db81-111">List all controllers in a subscription.</span></span>

### <span data-ttu-id="5db81-112">範例2</span><span class="sxs-lookup"><span data-stu-id="5db81-112">Example 2</span></span>
```powershell
PS C:\> Get-AzDevSpacesController --ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="5db81-113">在訂閱中取得 DevSpaces 控制器。</span><span class="sxs-lookup"><span data-stu-id="5db81-113">Get a DevSpaces controllers in a subscription.</span></span>

## <span data-ttu-id="5db81-114">參數</span><span class="sxs-lookup"><span data-stu-id="5db81-114">PARAMETERS</span></span>

### <span data-ttu-id="5db81-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5db81-115">-DefaultProfile</span></span>
<span data-ttu-id="5db81-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5db81-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5db81-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="5db81-117">-Name</span></span>
<span data-ttu-id="5db81-118">DevSpaces 控制器名稱。</span><span class="sxs-lookup"><span data-stu-id="5db81-118">DevSpaces controller name.</span></span>

```yaml
Type: System.String
Parameter Sets: DevSpacesControllerNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5db81-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5db81-119">-ResourceGroupName</span></span>
<span data-ttu-id="5db81-120">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="5db81-120">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ListDevSpacesControllerParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DevSpacesControllerNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5db81-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5db81-121">CommonParameters</span></span>
<span data-ttu-id="5db81-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5db81-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5db81-123">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5db81-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5db81-124">輸入</span><span class="sxs-lookup"><span data-stu-id="5db81-124">INPUTS</span></span>

### <span data-ttu-id="5db81-125">所有</span><span class="sxs-lookup"><span data-stu-id="5db81-125">None</span></span>

## <span data-ttu-id="5db81-126">輸出</span><span class="sxs-lookup"><span data-stu-id="5db81-126">OUTPUTS</span></span>

### <span data-ttu-id="5db81-127">PSController 中的 DevSpaces。</span><span class="sxs-lookup"><span data-stu-id="5db81-127">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="5db81-128">筆記</span><span class="sxs-lookup"><span data-stu-id="5db81-128">NOTES</span></span>

## <span data-ttu-id="5db81-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="5db81-129">RELATED LINKS</span></span>
