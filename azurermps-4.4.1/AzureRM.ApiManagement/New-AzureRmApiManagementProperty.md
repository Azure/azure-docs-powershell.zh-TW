---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A91F93D3-B8C7-4328-A049-AB9877C1166C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProperty.md
ms.openlocfilehash: cb50ea5735a9f63f5f35b8f1cb0648c566e6108d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625731"
---
# <span data-ttu-id="bd9fb-101">New-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="bd9fb-101">New-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="bd9fb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bd9fb-102">SYNOPSIS</span></span>
<span data-ttu-id="bd9fb-103">建立新的屬性。</span><span class="sxs-lookup"><span data-stu-id="bd9fb-103">Creates a new Property.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd9fb-104">句法</span><span class="sxs-lookup"><span data-stu-id="bd9fb-104">SYNTAX</span></span>

```
New-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>] -Name <String>
 -Value <String> [-Secret] [-Tags <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd9fb-105">說明</span><span class="sxs-lookup"><span data-stu-id="bd9fb-105">DESCRIPTION</span></span>
<span data-ttu-id="bd9fb-106">**新的-AzureRmApiManagementProperty** Cmdlet 會建立 Azure API 管理 **屬性** 。</span><span class="sxs-lookup"><span data-stu-id="bd9fb-106">The **New-AzureRmApiManagementProperty** cmdlet creates an Azure API Management **Property**.</span></span>

## <span data-ttu-id="bd9fb-107">示例</span><span class="sxs-lookup"><span data-stu-id="bd9fb-107">EXAMPLES</span></span>

### <span data-ttu-id="bd9fb-108">範例1：建立包含標記的屬性</span><span class="sxs-lookup"><span data-stu-id="bd9fb-108">Example 1: Create a property that includes tags</span></span>
```
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> New-AzureRmApiManagementProperty -Context $ApimContext -PropertyId "Property11" -Name "Property Name" -Value "Property Value" -Tags $Tags
```

<span data-ttu-id="bd9fb-109">第一個命令會將兩個值指派給 $Tags 變數。</span><span class="sxs-lookup"><span data-stu-id="bd9fb-109">The first command assigns two values to the $Tags variable.</span></span>

<span data-ttu-id="bd9fb-110">第二個命令會建立屬性，並將 $Tags 中的字串指定為屬性上的標記。</span><span class="sxs-lookup"><span data-stu-id="bd9fb-110">The second command creates a property and assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="bd9fb-111">範例2：建立具有機密值的屬性</span><span class="sxs-lookup"><span data-stu-id="bd9fb-111">Example 2: Create a property that has a secret value</span></span>
```
PS C:\>New-AzureRmApiManagementProperty -Context $apimContext -PropertyId "Property12" -Name "Secret Property -Value "Secret Property Value" -Secret
```

<span data-ttu-id="bd9fb-112">這個命令會建立具有已加密之值的 **屬性** 。</span><span class="sxs-lookup"><span data-stu-id="bd9fb-112">This command creates a **Property** that has a value that is encrypted.</span></span>

## <span data-ttu-id="bd9fb-113">參數</span><span class="sxs-lookup"><span data-stu-id="bd9fb-113">PARAMETERS</span></span>

### <span data-ttu-id="bd9fb-114">-內容</span><span class="sxs-lookup"><span data-stu-id="bd9fb-114">-Context</span></span>
<span data-ttu-id="bd9fb-115">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="bd9fb-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="bd9fb-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="bd9fb-116">-Name</span></span>
<span data-ttu-id="bd9fb-117">指定此 Cmdlet 所建立之屬性的名稱。</span><span class="sxs-lookup"><span data-stu-id="bd9fb-117">Specifies the name of the property that this cmdlet creates.</span></span>
<span data-ttu-id="bd9fb-118">最大長度為100個字元。</span><span class="sxs-lookup"><span data-stu-id="bd9fb-118">Maximum length is 100 characters.</span></span>
<span data-ttu-id="bd9fb-119">名稱只包含字母、數位、句點、破折號及底線字元。</span><span class="sxs-lookup"><span data-stu-id="bd9fb-119">Names contain only letters, digits, period, dash, and underscore characters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd9fb-120">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="bd9fb-120">-PropertyId</span></span>
<span data-ttu-id="bd9fb-121">指定屬性的識別碼。</span><span class="sxs-lookup"><span data-stu-id="bd9fb-121">Specifies an ID for the property.</span></span>
<span data-ttu-id="bd9fb-122">最大長度為256個字元。</span><span class="sxs-lookup"><span data-stu-id="bd9fb-122">Maximum length is 256 characters.</span></span>
<span data-ttu-id="bd9fb-123">如果您沒有指定識別碼，此 Cmdlet 會產生一個 ID。</span><span class="sxs-lookup"><span data-stu-id="bd9fb-123">If you do not specify an ID, this cmdlet generates one.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd9fb-124">密碼</span><span class="sxs-lookup"><span data-stu-id="bd9fb-124">-Secret</span></span>
<span data-ttu-id="bd9fb-125">表示屬性值是一個機密，應該經過加密。</span><span class="sxs-lookup"><span data-stu-id="bd9fb-125">Indicates that the property value is a secret and should be encrypted.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd9fb-126">-標記</span><span class="sxs-lookup"><span data-stu-id="bd9fb-126">-Tags</span></span>
<span data-ttu-id="bd9fb-127">指定此 Cmdlet 關聯至屬性的標記陣列。</span><span class="sxs-lookup"><span data-stu-id="bd9fb-127">Specifies an array of tags that this cmdlet associates to the property.</span></span>
<span data-ttu-id="bd9fb-128">您可以使用標記來篩選屬性清單。</span><span class="sxs-lookup"><span data-stu-id="bd9fb-128">You can use tags to filter the property list.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd9fb-129">-值</span><span class="sxs-lookup"><span data-stu-id="bd9fb-129">-Value</span></span>
<span data-ttu-id="bd9fb-130">指定屬性的值。</span><span class="sxs-lookup"><span data-stu-id="bd9fb-130">Specifies a value for the property.</span></span>
<span data-ttu-id="bd9fb-131">這個值可以包含原則運算式。</span><span class="sxs-lookup"><span data-stu-id="bd9fb-131">This value can contain policy expressions.</span></span>
<span data-ttu-id="bd9fb-132">最大長度為1000個字元。</span><span class="sxs-lookup"><span data-stu-id="bd9fb-132">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="bd9fb-133">此值可能不是空白，或是只由空格所組成。</span><span class="sxs-lookup"><span data-stu-id="bd9fb-133">The value may not be empty or consist only of whitespace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd9fb-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd9fb-134">-DefaultProfile</span></span>
<span data-ttu-id="bd9fb-135">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bd9fb-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd9fb-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd9fb-136">CommonParameters</span></span>
<span data-ttu-id="bd9fb-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bd9fb-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd9fb-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bd9fb-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd9fb-139">輸入</span><span class="sxs-lookup"><span data-stu-id="bd9fb-139">INPUTS</span></span>

## <span data-ttu-id="bd9fb-140">輸出</span><span class="sxs-lookup"><span data-stu-id="bd9fb-140">OUTPUTS</span></span>

### <span data-ttu-id="bd9fb-141">ServiceManagement. PsApiManagementProperty （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="bd9fb-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="bd9fb-142">筆記</span><span class="sxs-lookup"><span data-stu-id="bd9fb-142">NOTES</span></span>

## <span data-ttu-id="bd9fb-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="bd9fb-143">RELATED LINKS</span></span>

[<span data-ttu-id="bd9fb-144">移除-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="bd9fb-144">Remove-AzureRmApiManagementProperty</span></span>](./Remove-AzureRmApiManagementProperty.md)

[<span data-ttu-id="bd9fb-145">Set-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="bd9fb-145">Set-AzureRmApiManagementProperty</span></span>](./Set-AzureRmApiManagementProperty.md)


