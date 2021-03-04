---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementresourcelocationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementResourceLocationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementResourceLocationObject.md
ms.openlocfilehash: 88b2ae64430f73df242d7003baa2c72ec6512dce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904546"
---
# <span data-ttu-id="73419-101">New-AzApiManagementResourceLocationObject</span><span class="sxs-lookup"><span data-stu-id="73419-101">New-AzApiManagementResourceLocationObject</span></span>

## <span data-ttu-id="73419-102">簡介</span><span class="sxs-lookup"><span data-stu-id="73419-102">SYNOPSIS</span></span>
<span data-ttu-id="73419-103">建立新資源位置合約 (閘道中) 。</span><span class="sxs-lookup"><span data-stu-id="73419-103">Create a new resource location contract (used in Gateways).</span></span>

## <span data-ttu-id="73419-104">語法</span><span class="sxs-lookup"><span data-stu-id="73419-104">SYNTAX</span></span>

```
New-AzApiManagementResourceLocationObject -Name <String> [-City <String>] [-District <String>]
 [-CountryOrRegion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73419-105">描述</span><span class="sxs-lookup"><span data-stu-id="73419-105">DESCRIPTION</span></span>
<span data-ttu-id="73419-106">**New-AzApiManagementResourceLocationObject** Cmdlet 會建立新資源位置合約， (閘道) 。</span><span class="sxs-lookup"><span data-stu-id="73419-106">The **New-AzApiManagementResourceLocationObject** cmdlet create a new resource location contract (used in Gateways).</span></span>

## <span data-ttu-id="73419-107">例子</span><span class="sxs-lookup"><span data-stu-id="73419-107">EXAMPLES</span></span>

### <span data-ttu-id="73419-108">範例 1：建立資源位置合約</span><span class="sxs-lookup"><span data-stu-id="73419-108">Example 1: Create a resource location contract</span></span>
```powershell
PS C:\>$location = New-AzApiManagementResourceLocationObject -Name "n1" -City "c1" -District "d1" -CountryOrRegion "r1"
```

<span data-ttu-id="73419-109">此命令會建立資源位置。</span><span class="sxs-lookup"><span data-stu-id="73419-109">This command creates a resource location.</span></span>

## <span data-ttu-id="73419-110">參數</span><span class="sxs-lookup"><span data-stu-id="73419-110">PARAMETERS</span></span>

### <span data-ttu-id="73419-111">-縣/市</span><span class="sxs-lookup"><span data-stu-id="73419-111">-City</span></span>
<span data-ttu-id="73419-112">位置城市。</span><span class="sxs-lookup"><span data-stu-id="73419-112">Location City.</span></span>
<span data-ttu-id="73419-113">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="73419-113">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73419-114">-CountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="73419-114">-CountryOrRegion</span></span>
<span data-ttu-id="73419-115">位置國家/地區或地區。</span><span class="sxs-lookup"><span data-stu-id="73419-115">Location Country or Region.</span></span>
<span data-ttu-id="73419-116">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="73419-116">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73419-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73419-117">-DefaultProfile</span></span>
<span data-ttu-id="73419-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="73419-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73419-119">-地區</span><span class="sxs-lookup"><span data-stu-id="73419-119">-District</span></span>
<span data-ttu-id="73419-120">位置區。</span><span class="sxs-lookup"><span data-stu-id="73419-120">Location District.</span></span>
<span data-ttu-id="73419-121">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="73419-121">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73419-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="73419-122">-Name</span></span>
<span data-ttu-id="73419-123">位置名稱。</span><span class="sxs-lookup"><span data-stu-id="73419-123">Location Name.</span></span>
<span data-ttu-id="73419-124">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="73419-124">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73419-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73419-125">CommonParameters</span></span>
<span data-ttu-id="73419-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="73419-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73419-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="73419-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73419-128">輸入</span><span class="sxs-lookup"><span data-stu-id="73419-128">INPUTS</span></span>

### <span data-ttu-id="73419-129">沒有</span><span class="sxs-lookup"><span data-stu-id="73419-129">None</span></span>

## <span data-ttu-id="73419-130">輸出</span><span class="sxs-lookup"><span data-stu-id="73419-130">OUTPUTS</span></span>

### <span data-ttu-id="73419-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementResourceLocation</span><span class="sxs-lookup"><span data-stu-id="73419-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span></span>

## <span data-ttu-id="73419-132">筆記</span><span class="sxs-lookup"><span data-stu-id="73419-132">NOTES</span></span>

## <span data-ttu-id="73419-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="73419-133">RELATED LINKS</span></span>
