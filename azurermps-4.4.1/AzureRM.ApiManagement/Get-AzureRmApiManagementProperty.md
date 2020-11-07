---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 894297BF-2771-4871-9E4C-8684364DAC4B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProperty.md
ms.openlocfilehash: 7542e9621d90ffdb19bb8db679592dd17a216d5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624225"
---
# <span data-ttu-id="65d0e-101">Get-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="65d0e-101">Get-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="65d0e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="65d0e-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65d0e-103">句法</span><span class="sxs-lookup"><span data-stu-id="65d0e-103">SYNTAX</span></span>

### <span data-ttu-id="65d0e-104">取得預設)  (的所有屬性</span><span class="sxs-lookup"><span data-stu-id="65d0e-104">Get all properties (Default)</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="65d0e-105">透過屬性識別碼取得</span><span class="sxs-lookup"><span data-stu-id="65d0e-105">Get by property ID</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65d0e-106">尋找包含名稱的屬性</span><span class="sxs-lookup"><span data-stu-id="65d0e-106">Find properties containing Name</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65d0e-107">依標記尋找屬性</span><span class="sxs-lookup"><span data-stu-id="65d0e-107">Find properties by Tag</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-Tag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65d0e-108">說明</span><span class="sxs-lookup"><span data-stu-id="65d0e-108">DESCRIPTION</span></span>

## <span data-ttu-id="65d0e-109">示例</span><span class="sxs-lookup"><span data-stu-id="65d0e-109">EXAMPLES</span></span>

### <span data-ttu-id="65d0e-110">sr-1</span><span class="sxs-lookup"><span data-stu-id="65d0e-110">1:</span></span>
```
PS C:\> Get-AzureRmApiManagementProperty -Context $Context -Name $PropertyName
```

## <span data-ttu-id="65d0e-111">參數</span><span class="sxs-lookup"><span data-stu-id="65d0e-111">PARAMETERS</span></span>

### <span data-ttu-id="65d0e-112">-內容</span><span class="sxs-lookup"><span data-stu-id="65d0e-112">-Context</span></span>
```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65d0e-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="65d0e-113">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: Find properties containing Name
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65d0e-114">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="65d0e-114">-PropertyId</span></span>
```yaml
Type: System.String
Parameter Sets: Get by property ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65d0e-115">-Tag</span><span class="sxs-lookup"><span data-stu-id="65d0e-115">-Tag</span></span>
<span data-ttu-id="65d0e-116">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="65d0e-116">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="65d0e-117">例如：</span><span class="sxs-lookup"><span data-stu-id="65d0e-117">For example:</span></span>

<span data-ttu-id="65d0e-118">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="65d0e-118">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.String
Parameter Sets: Find properties by Tag
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65d0e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65d0e-119">-DefaultProfile</span></span>
<span data-ttu-id="65d0e-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="65d0e-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65d0e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65d0e-121">CommonParameters</span></span>
<span data-ttu-id="65d0e-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="65d0e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65d0e-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="65d0e-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65d0e-124">輸入</span><span class="sxs-lookup"><span data-stu-id="65d0e-124">INPUTS</span></span>

## <span data-ttu-id="65d0e-125">輸出</span><span class="sxs-lookup"><span data-stu-id="65d0e-125">OUTPUTS</span></span>

### <span data-ttu-id="65d0e-126">[System.object]. ApiManagement [ServiceManagement]。 PsApiManagementProperty] （]）</span><span class="sxs-lookup"><span data-stu-id="65d0e-126">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty]</span></span>

### <span data-ttu-id="65d0e-127">ServiceManagement. PsApiManagementProperty （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="65d0e-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="65d0e-128">筆記</span><span class="sxs-lookup"><span data-stu-id="65d0e-128">NOTES</span></span>

## <span data-ttu-id="65d0e-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="65d0e-129">RELATED LINKS</span></span>

