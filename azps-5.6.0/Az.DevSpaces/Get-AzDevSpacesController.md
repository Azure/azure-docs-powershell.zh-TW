---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/powershell/module/az.devspaces/get-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Get-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Get-AzDevSpacesController.md
ms.openlocfilehash: dd7ba99632cfef493fe3202b2402a938b11fa807
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904113"
---
# <span data-ttu-id="fc95b-101">Get-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="fc95b-101">Get-AzDevSpacesController</span></span>

## <span data-ttu-id="fc95b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="fc95b-102">SYNOPSIS</span></span>
<span data-ttu-id="fc95b-103">取得或列出 Azure DevSpaces 控制器。</span><span class="sxs-lookup"><span data-stu-id="fc95b-103">Get or list Azure DevSpaces controller.</span></span>

## <span data-ttu-id="fc95b-104">語法</span><span class="sxs-lookup"><span data-stu-id="fc95b-104">SYNTAX</span></span>

### <span data-ttu-id="fc95b-105">ListDevSpacesControllerParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="fc95b-105">ListDevSpacesControllerParameterSet (Default)</span></span>
```
Get-AzDevSpacesController [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fc95b-106">DevSpacesControllerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc95b-106">DevSpacesControllerNameParameterSet</span></span>
```
Get-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc95b-107">描述</span><span class="sxs-lookup"><span data-stu-id="fc95b-107">DESCRIPTION</span></span>
<span data-ttu-id="fc95b-108">取得或列出 Azure DevSpaces 控制器。</span><span class="sxs-lookup"><span data-stu-id="fc95b-108">Get or list Azure DevSpaces controller.</span></span>

## <span data-ttu-id="fc95b-109">例子</span><span class="sxs-lookup"><span data-stu-id="fc95b-109">EXAMPLES</span></span>

### <span data-ttu-id="fc95b-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="fc95b-110">Example 1</span></span>
```powershell
PS C:\> Get-AzDevSpacesController

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="fc95b-111">列出訂閱中所有的控制器。</span><span class="sxs-lookup"><span data-stu-id="fc95b-111">List all controllers in a subscription.</span></span>

### <span data-ttu-id="fc95b-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="fc95b-112">Example 2</span></span>
```powershell
PS C:\> Get-AzDevSpacesController --ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="fc95b-113">取得訂閱中的 DevSpaces 控制器。</span><span class="sxs-lookup"><span data-stu-id="fc95b-113">Get a DevSpaces controllers in a subscription.</span></span>

## <span data-ttu-id="fc95b-114">參數</span><span class="sxs-lookup"><span data-stu-id="fc95b-114">PARAMETERS</span></span>

### <span data-ttu-id="fc95b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc95b-115">-DefaultProfile</span></span>
<span data-ttu-id="fc95b-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="fc95b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc95b-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="fc95b-117">-Name</span></span>
<span data-ttu-id="fc95b-118">DevSpaces 控制器名稱。</span><span class="sxs-lookup"><span data-stu-id="fc95b-118">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="fc95b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc95b-119">-ResourceGroupName</span></span>
<span data-ttu-id="fc95b-120">資源組名</span><span class="sxs-lookup"><span data-stu-id="fc95b-120">Resource group name</span></span>

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

### <span data-ttu-id="fc95b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc95b-121">CommonParameters</span></span>
<span data-ttu-id="fc95b-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="fc95b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc95b-123">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="fc95b-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc95b-124">輸入</span><span class="sxs-lookup"><span data-stu-id="fc95b-124">INPUTS</span></span>

### <span data-ttu-id="fc95b-125">沒有</span><span class="sxs-lookup"><span data-stu-id="fc95b-125">None</span></span>

## <span data-ttu-id="fc95b-126">輸出</span><span class="sxs-lookup"><span data-stu-id="fc95b-126">OUTPUTS</span></span>

### <span data-ttu-id="fc95b-127">Microsoft.Azure.Commands.DevSpaces.models.PSController</span><span class="sxs-lookup"><span data-stu-id="fc95b-127">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="fc95b-128">筆記</span><span class="sxs-lookup"><span data-stu-id="fc95b-128">NOTES</span></span>

## <span data-ttu-id="fc95b-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="fc95b-129">RELATED LINKS</span></span>
