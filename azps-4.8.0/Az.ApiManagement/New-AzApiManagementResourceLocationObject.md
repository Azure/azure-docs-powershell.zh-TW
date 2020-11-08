---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementresourcelocationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementResourceLocationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementResourceLocationObject.md
ms.openlocfilehash: 505264809b513ad144fa3812193fc39f86ab9b1e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970681"
---
# <span data-ttu-id="a2408-101">New-AzApiManagementResourceLocationObject</span><span class="sxs-lookup"><span data-stu-id="a2408-101">New-AzApiManagementResourceLocationObject</span></span>

## <span data-ttu-id="a2408-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a2408-102">SYNOPSIS</span></span>
<span data-ttu-id="a2408-103">建立新的資源位置合約 (在閘道) 中使用。</span><span class="sxs-lookup"><span data-stu-id="a2408-103">Create a new resource location contract (used in Gateways).</span></span>

## <span data-ttu-id="a2408-104">句法</span><span class="sxs-lookup"><span data-stu-id="a2408-104">SYNTAX</span></span>

```
New-AzApiManagementResourceLocationObject -Name <String> [-City <String>] [-District <String>]
 [-CountryOrRegion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2408-105">說明</span><span class="sxs-lookup"><span data-stu-id="a2408-105">DESCRIPTION</span></span>
<span data-ttu-id="a2408-106">**新的-AzApiManagementResourceLocationObject** Cmdlet 會建立新的資源位置合約 (用在閘道) 中。</span><span class="sxs-lookup"><span data-stu-id="a2408-106">The **New-AzApiManagementResourceLocationObject** cmdlet create a new resource location contract (used in Gateways).</span></span>

## <span data-ttu-id="a2408-107">示例</span><span class="sxs-lookup"><span data-stu-id="a2408-107">EXAMPLES</span></span>

### <span data-ttu-id="a2408-108">範例1：建立資源位置合約</span><span class="sxs-lookup"><span data-stu-id="a2408-108">Example 1: Create a resource location contract</span></span>
```powershell
PS C:\>$location = New-AzApiManagementResourceLocationObject -Name "n1" -City "c1" -District "d1" -CountryOrRegion "r1"
```

<span data-ttu-id="a2408-109">這個命令會建立資源位置。</span><span class="sxs-lookup"><span data-stu-id="a2408-109">This command creates a resource location.</span></span>

## <span data-ttu-id="a2408-110">參數</span><span class="sxs-lookup"><span data-stu-id="a2408-110">PARAMETERS</span></span>

### <span data-ttu-id="a2408-111">-城市</span><span class="sxs-lookup"><span data-stu-id="a2408-111">-City</span></span>
<span data-ttu-id="a2408-112">位置城市。</span><span class="sxs-lookup"><span data-stu-id="a2408-112">Location City.</span></span>
<span data-ttu-id="a2408-113">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="a2408-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="a2408-114">-CountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="a2408-114">-CountryOrRegion</span></span>
<span data-ttu-id="a2408-115">國家或地區的位置。</span><span class="sxs-lookup"><span data-stu-id="a2408-115">Location Country or Region.</span></span>
<span data-ttu-id="a2408-116">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="a2408-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="a2408-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2408-117">-DefaultProfile</span></span>
<span data-ttu-id="a2408-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a2408-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2408-119">-地區</span><span class="sxs-lookup"><span data-stu-id="a2408-119">-District</span></span>
<span data-ttu-id="a2408-120">位置地區。</span><span class="sxs-lookup"><span data-stu-id="a2408-120">Location District.</span></span>
<span data-ttu-id="a2408-121">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="a2408-121">This parameter is optional.</span></span>

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

### <span data-ttu-id="a2408-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="a2408-122">-Name</span></span>
<span data-ttu-id="a2408-123">位置名稱。</span><span class="sxs-lookup"><span data-stu-id="a2408-123">Location Name.</span></span>
<span data-ttu-id="a2408-124">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="a2408-124">This parameter is required.</span></span>

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

### <span data-ttu-id="a2408-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2408-125">CommonParameters</span></span>
<span data-ttu-id="a2408-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a2408-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2408-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a2408-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2408-128">輸入</span><span class="sxs-lookup"><span data-stu-id="a2408-128">INPUTS</span></span>

### <span data-ttu-id="a2408-129">所有</span><span class="sxs-lookup"><span data-stu-id="a2408-129">None</span></span>

## <span data-ttu-id="a2408-130">輸出</span><span class="sxs-lookup"><span data-stu-id="a2408-130">OUTPUTS</span></span>

### <span data-ttu-id="a2408-131">ServiceManagement. PsApiManagementResourceLocation （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="a2408-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span></span>

## <span data-ttu-id="a2408-132">筆記</span><span class="sxs-lookup"><span data-stu-id="a2408-132">NOTES</span></span>

## <span data-ttu-id="a2408-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="a2408-133">RELATED LINKS</span></span>