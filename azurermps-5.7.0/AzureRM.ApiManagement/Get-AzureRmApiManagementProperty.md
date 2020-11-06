---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 894297BF-2771-4871-9E4C-8684364DAC4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProperty.md
ms.openlocfilehash: 47167e0729ab3476c74124e16d6ae95901f57ad2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448802"
---
# <span data-ttu-id="3bd5b-101">Get-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="3bd5b-101">Get-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="3bd5b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3bd5b-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3bd5b-103">句法</span><span class="sxs-lookup"><span data-stu-id="3bd5b-103">SYNTAX</span></span>

### <span data-ttu-id="3bd5b-104">GetAllProperties (預設) </span><span class="sxs-lookup"><span data-stu-id="3bd5b-104">GetAllProperties (Default)</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3bd5b-105">GetByPropertyId</span><span class="sxs-lookup"><span data-stu-id="3bd5b-105">GetByPropertyId</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3bd5b-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="3bd5b-106">GetByName</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3bd5b-107">GetByTag</span><span class="sxs-lookup"><span data-stu-id="3bd5b-107">GetByTag</span></span>
```
Get-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-Tag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3bd5b-108">說明</span><span class="sxs-lookup"><span data-stu-id="3bd5b-108">DESCRIPTION</span></span>

## <span data-ttu-id="3bd5b-109">示例</span><span class="sxs-lookup"><span data-stu-id="3bd5b-109">EXAMPLES</span></span>

### <span data-ttu-id="3bd5b-110">範例1：透過名稱取得屬性</span><span class="sxs-lookup"><span data-stu-id="3bd5b-110">Example 1: Get Property by name</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementProperty -Context $apimContext -Name "sql-connectionstring"
```

## <span data-ttu-id="3bd5b-111">參數</span><span class="sxs-lookup"><span data-stu-id="3bd5b-111">PARAMETERS</span></span>

### <span data-ttu-id="3bd5b-112">-內容</span><span class="sxs-lookup"><span data-stu-id="3bd5b-112">-Context</span></span>
```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bd5b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bd5b-113">-DefaultProfile</span></span>
<span data-ttu-id="3bd5b-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3bd5b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bd5b-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="3bd5b-115">-Name</span></span>
```yaml
Type: String
Parameter Sets: GetByName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bd5b-116">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="3bd5b-116">-PropertyId</span></span>
```yaml
Type: String
Parameter Sets: GetByPropertyId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bd5b-117">-Tag</span><span class="sxs-lookup"><span data-stu-id="3bd5b-117">-Tag</span></span>
<span data-ttu-id="3bd5b-118">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="3bd5b-118">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3bd5b-119">例如：</span><span class="sxs-lookup"><span data-stu-id="3bd5b-119">For example:</span></span>

<span data-ttu-id="3bd5b-120">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="3bd5b-120">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: String
Parameter Sets: GetByTag
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bd5b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bd5b-121">CommonParameters</span></span>
<span data-ttu-id="3bd5b-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3bd5b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bd5b-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3bd5b-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bd5b-124">輸入</span><span class="sxs-lookup"><span data-stu-id="3bd5b-124">INPUTS</span></span>

### <span data-ttu-id="3bd5b-125">所有</span><span class="sxs-lookup"><span data-stu-id="3bd5b-125">None</span></span>
<span data-ttu-id="3bd5b-126">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="3bd5b-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3bd5b-127">輸出</span><span class="sxs-lookup"><span data-stu-id="3bd5b-127">OUTPUTS</span></span>

### <span data-ttu-id="3bd5b-128">[System.object]. ApiManagement [ServiceManagement]。 PsApiManagementProperty] （]）</span><span class="sxs-lookup"><span data-stu-id="3bd5b-128">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty]</span></span>

### <span data-ttu-id="3bd5b-129">ServiceManagement. PsApiManagementProperty （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="3bd5b-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="3bd5b-130">筆記</span><span class="sxs-lookup"><span data-stu-id="3bd5b-130">NOTES</span></span>

## <span data-ttu-id="3bd5b-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="3bd5b-131">RELATED LINKS</span></span>

