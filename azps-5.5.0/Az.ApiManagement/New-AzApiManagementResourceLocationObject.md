---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementresourcelocationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementResourceLocationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementResourceLocationObject.md
ms.openlocfilehash: 505264809b513ad144fa3812193fc39f86ab9b1e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100141678"
---
# <span data-ttu-id="ab994-101">New-AzApiManagementResourceLocationObject</span><span class="sxs-lookup"><span data-stu-id="ab994-101">New-AzApiManagementResourceLocationObject</span></span>

## <span data-ttu-id="ab994-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ab994-102">SYNOPSIS</span></span>
<span data-ttu-id="ab994-103">建立新的資源位置合約 (在閘道) 中使用。</span><span class="sxs-lookup"><span data-stu-id="ab994-103">Create a new resource location contract (used in Gateways).</span></span>

## <span data-ttu-id="ab994-104">句法</span><span class="sxs-lookup"><span data-stu-id="ab994-104">SYNTAX</span></span>

```
New-AzApiManagementResourceLocationObject -Name <String> [-City <String>] [-District <String>]
 [-CountryOrRegion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab994-105">說明</span><span class="sxs-lookup"><span data-stu-id="ab994-105">DESCRIPTION</span></span>
<span data-ttu-id="ab994-106">**新的-AzApiManagementResourceLocationObject** Cmdlet 會建立新的資源位置合約 (用在閘道) 中。</span><span class="sxs-lookup"><span data-stu-id="ab994-106">The **New-AzApiManagementResourceLocationObject** cmdlet create a new resource location contract (used in Gateways).</span></span>

## <span data-ttu-id="ab994-107">示例</span><span class="sxs-lookup"><span data-stu-id="ab994-107">EXAMPLES</span></span>

### <span data-ttu-id="ab994-108">範例1：建立資源位置合約</span><span class="sxs-lookup"><span data-stu-id="ab994-108">Example 1: Create a resource location contract</span></span>
```powershell
PS C:\>$location = New-AzApiManagementResourceLocationObject -Name "n1" -City "c1" -District "d1" -CountryOrRegion "r1"
```

<span data-ttu-id="ab994-109">這個命令會建立資源位置。</span><span class="sxs-lookup"><span data-stu-id="ab994-109">This command creates a resource location.</span></span>

## <span data-ttu-id="ab994-110">參數</span><span class="sxs-lookup"><span data-stu-id="ab994-110">PARAMETERS</span></span>

### <span data-ttu-id="ab994-111">-城市</span><span class="sxs-lookup"><span data-stu-id="ab994-111">-City</span></span>
<span data-ttu-id="ab994-112">位置城市。</span><span class="sxs-lookup"><span data-stu-id="ab994-112">Location City.</span></span>
<span data-ttu-id="ab994-113">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="ab994-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="ab994-114">-CountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="ab994-114">-CountryOrRegion</span></span>
<span data-ttu-id="ab994-115">國家或地區的位置。</span><span class="sxs-lookup"><span data-stu-id="ab994-115">Location Country or Region.</span></span>
<span data-ttu-id="ab994-116">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="ab994-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="ab994-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab994-117">-DefaultProfile</span></span>
<span data-ttu-id="ab994-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ab994-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab994-119">-地區</span><span class="sxs-lookup"><span data-stu-id="ab994-119">-District</span></span>
<span data-ttu-id="ab994-120">位置地區。</span><span class="sxs-lookup"><span data-stu-id="ab994-120">Location District.</span></span>
<span data-ttu-id="ab994-121">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="ab994-121">This parameter is optional.</span></span>

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

### <span data-ttu-id="ab994-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="ab994-122">-Name</span></span>
<span data-ttu-id="ab994-123">位置名稱。</span><span class="sxs-lookup"><span data-stu-id="ab994-123">Location Name.</span></span>
<span data-ttu-id="ab994-124">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="ab994-124">This parameter is required.</span></span>

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

### <span data-ttu-id="ab994-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab994-125">CommonParameters</span></span>
<span data-ttu-id="ab994-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ab994-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab994-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ab994-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab994-128">輸入</span><span class="sxs-lookup"><span data-stu-id="ab994-128">INPUTS</span></span>

### <span data-ttu-id="ab994-129">所有</span><span class="sxs-lookup"><span data-stu-id="ab994-129">None</span></span>

## <span data-ttu-id="ab994-130">輸出</span><span class="sxs-lookup"><span data-stu-id="ab994-130">OUTPUTS</span></span>

### <span data-ttu-id="ab994-131">ServiceManagement. PsApiManagementResourceLocation （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="ab994-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span></span>

## <span data-ttu-id="ab994-132">筆記</span><span class="sxs-lookup"><span data-stu-id="ab994-132">NOTES</span></span>

## <span data-ttu-id="ab994-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="ab994-133">RELATED LINKS</span></span>
