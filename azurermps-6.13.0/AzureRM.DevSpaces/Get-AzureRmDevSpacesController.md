---
external help file: Microsoft.Azure.Commands.DevSpaces.dll-Help.xml
Module Name: AzureRM.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devspaces/get-azureevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevSpaces/Commands.DevSpaces/help/Get-AzureRmDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevSpaces/Commands.DevSpaces/help/Get-AzureRmDevSpacesController.md
ms.openlocfilehash: d0140af9d5345e9f3f68c212ae43403fc0f64280
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448443"
---
# <span data-ttu-id="55fba-101">Get-AzureRmDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="55fba-101">Get-AzureRmDevSpacesController</span></span>

## <span data-ttu-id="55fba-102">摘要</span><span class="sxs-lookup"><span data-stu-id="55fba-102">SYNOPSIS</span></span>
<span data-ttu-id="55fba-103">取得或列出 Azure DevSpaces 控制器。</span><span class="sxs-lookup"><span data-stu-id="55fba-103">Get or list Azure DevSpaces controller.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55fba-104">句法</span><span class="sxs-lookup"><span data-stu-id="55fba-104">SYNTAX</span></span>

### <span data-ttu-id="55fba-105">ListDevSpacesControllerParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="55fba-105">ListDevSpacesControllerParameterSet (Default)</span></span>
```
Get-AzureRmDevSpacesController [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="55fba-106">DevSpacesControllerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="55fba-106">DevSpacesControllerNameParameterSet</span></span>
```
Get-AzureRmDevSpacesController [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55fba-107">說明</span><span class="sxs-lookup"><span data-stu-id="55fba-107">DESCRIPTION</span></span>
<span data-ttu-id="55fba-108">取得或列出 Azure DevSpaces 控制器。</span><span class="sxs-lookup"><span data-stu-id="55fba-108">Get or list Azure DevSpaces controller.</span></span>

## <span data-ttu-id="55fba-109">示例</span><span class="sxs-lookup"><span data-stu-id="55fba-109">EXAMPLES</span></span>

### <span data-ttu-id="55fba-110">範例1</span><span class="sxs-lookup"><span data-stu-id="55fba-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDevSpacesController

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="55fba-111">列出訂閱中的所有控制器。</span><span class="sxs-lookup"><span data-stu-id="55fba-111">List all controllers in a subscription.</span></span>

### <span data-ttu-id="55fba-112">範例2</span><span class="sxs-lookup"><span data-stu-id="55fba-112">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmDevSpacesController --ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="55fba-113">在訂閱中取得 DevSpaces 控制器。</span><span class="sxs-lookup"><span data-stu-id="55fba-113">Get a DevSpaces controllers in a subscription.</span></span>

## <span data-ttu-id="55fba-114">參數</span><span class="sxs-lookup"><span data-stu-id="55fba-114">PARAMETERS</span></span>

### <span data-ttu-id="55fba-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55fba-115">-DefaultProfile</span></span>
<span data-ttu-id="55fba-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="55fba-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55fba-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="55fba-117">-Name</span></span>
<span data-ttu-id="55fba-118">DevSpaces 控制器名稱。</span><span class="sxs-lookup"><span data-stu-id="55fba-118">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="55fba-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55fba-119">-ResourceGroupName</span></span>
<span data-ttu-id="55fba-120">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="55fba-120">Resource group name</span></span>

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

### <span data-ttu-id="55fba-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55fba-121">CommonParameters</span></span>
<span data-ttu-id="55fba-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="55fba-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55fba-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="55fba-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55fba-124">輸入</span><span class="sxs-lookup"><span data-stu-id="55fba-124">INPUTS</span></span>

### <span data-ttu-id="55fba-125">所有</span><span class="sxs-lookup"><span data-stu-id="55fba-125">None</span></span>

## <span data-ttu-id="55fba-126">輸出</span><span class="sxs-lookup"><span data-stu-id="55fba-126">OUTPUTS</span></span>

### <span data-ttu-id="55fba-127">PSController 中的 DevSpaces。</span><span class="sxs-lookup"><span data-stu-id="55fba-127">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="55fba-128">筆記</span><span class="sxs-lookup"><span data-stu-id="55fba-128">NOTES</span></span>

## <span data-ttu-id="55fba-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="55fba-129">RELATED LINKS</span></span>
