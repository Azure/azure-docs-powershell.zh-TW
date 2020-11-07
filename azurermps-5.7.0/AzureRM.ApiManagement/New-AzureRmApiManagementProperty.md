---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A91F93D3-B8C7-4328-A049-AB9877C1166C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProperty.md
ms.openlocfilehash: 55ef0d4ef714c1d434915def403f5560244a3697
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626577"
---
# <span data-ttu-id="0226a-101">New-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="0226a-101">New-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="0226a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0226a-102">SYNOPSIS</span></span>
<span data-ttu-id="0226a-103">建立新的屬性。</span><span class="sxs-lookup"><span data-stu-id="0226a-103">Creates a new Property.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0226a-104">句法</span><span class="sxs-lookup"><span data-stu-id="0226a-104">SYNTAX</span></span>

```
New-AzureRmApiManagementProperty -Context <PsApiManagementContext> [-PropertyId <String>] -Name <String>
 -Value <String> [-Secret] [-Tag <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0226a-105">說明</span><span class="sxs-lookup"><span data-stu-id="0226a-105">DESCRIPTION</span></span>
<span data-ttu-id="0226a-106">**新的-AzureRmApiManagementProperty** Cmdlet 會建立 Azure API 管理 **屬性** 。</span><span class="sxs-lookup"><span data-stu-id="0226a-106">The **New-AzureRmApiManagementProperty** cmdlet creates an Azure API Management **Property**.</span></span>

## <span data-ttu-id="0226a-107">示例</span><span class="sxs-lookup"><span data-stu-id="0226a-107">EXAMPLES</span></span>

### <span data-ttu-id="0226a-108">範例1：建立包含標記的屬性</span><span class="sxs-lookup"><span data-stu-id="0226a-108">Example 1: Create a property that includes tags</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> New-AzureRmApiManagementProperty -Context $apimContext -PropertyId "Property11" -Name "Property Name" -Value "Property Value" -Tags $Tags
```

<span data-ttu-id="0226a-109">第一個命令會將兩個值指派給 $Tags 變數。</span><span class="sxs-lookup"><span data-stu-id="0226a-109">The first command assigns two values to the $Tags variable.</span></span>

<span data-ttu-id="0226a-110">第二個命令會建立屬性，並將 $Tags 中的字串指定為屬性上的標記。</span><span class="sxs-lookup"><span data-stu-id="0226a-110">The second command creates a property and assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="0226a-111">範例2：建立具有機密值的屬性</span><span class="sxs-lookup"><span data-stu-id="0226a-111">Example 2: Create a property that has a secret value</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementProperty -Context $apimContext -PropertyId "Property12" -Name "Secret Property -Value "Secret Property Value" -Secret
```

<span data-ttu-id="0226a-112">這個命令會建立具有已加密之值的 **屬性** 。</span><span class="sxs-lookup"><span data-stu-id="0226a-112">This command creates a **Property** that has a value that is encrypted.</span></span>

## <span data-ttu-id="0226a-113">參數</span><span class="sxs-lookup"><span data-stu-id="0226a-113">PARAMETERS</span></span>

### <span data-ttu-id="0226a-114">-內容</span><span class="sxs-lookup"><span data-stu-id="0226a-114">-Context</span></span>
<span data-ttu-id="0226a-115">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="0226a-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="0226a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0226a-116">-DefaultProfile</span></span>
<span data-ttu-id="0226a-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0226a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="0226a-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="0226a-118">-Name</span></span>
<span data-ttu-id="0226a-119">指定此 Cmdlet 所建立之屬性的名稱。</span><span class="sxs-lookup"><span data-stu-id="0226a-119">Specifies the name of the property that this cmdlet creates.</span></span>
<span data-ttu-id="0226a-120">最大長度為100個字元。</span><span class="sxs-lookup"><span data-stu-id="0226a-120">Maximum length is 100 characters.</span></span>
<span data-ttu-id="0226a-121">名稱只包含字母、數位、句點、破折號及底線字元。</span><span class="sxs-lookup"><span data-stu-id="0226a-121">Names contain only letters, digits, period, dash, and underscore characters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0226a-122">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="0226a-122">-PropertyId</span></span>
<span data-ttu-id="0226a-123">指定屬性的識別碼。</span><span class="sxs-lookup"><span data-stu-id="0226a-123">Specifies an ID for the property.</span></span>
<span data-ttu-id="0226a-124">最大長度為256個字元。</span><span class="sxs-lookup"><span data-stu-id="0226a-124">Maximum length is 256 characters.</span></span>
<span data-ttu-id="0226a-125">如果您沒有指定識別碼，此 Cmdlet 會產生一個 ID。</span><span class="sxs-lookup"><span data-stu-id="0226a-125">If you do not specify an ID, this cmdlet generates one.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0226a-126">密碼</span><span class="sxs-lookup"><span data-stu-id="0226a-126">-Secret</span></span>
<span data-ttu-id="0226a-127">表示屬性值是一個機密，應該經過加密。</span><span class="sxs-lookup"><span data-stu-id="0226a-127">Indicates that the property value is a secret and should be encrypted.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0226a-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="0226a-128">-Tag</span></span>
<span data-ttu-id="0226a-129">要與屬性相關聯的標記。</span><span class="sxs-lookup"><span data-stu-id="0226a-129">Tags to be associated with Property.</span></span> <span data-ttu-id="0226a-130">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="0226a-130">This parameter is optional.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0226a-131">-值</span><span class="sxs-lookup"><span data-stu-id="0226a-131">-Value</span></span>
<span data-ttu-id="0226a-132">指定屬性的值。</span><span class="sxs-lookup"><span data-stu-id="0226a-132">Specifies a value for the property.</span></span>
<span data-ttu-id="0226a-133">這個值可以包含原則運算式。</span><span class="sxs-lookup"><span data-stu-id="0226a-133">This value can contain policy expressions.</span></span>
<span data-ttu-id="0226a-134">最大長度為1000個字元。</span><span class="sxs-lookup"><span data-stu-id="0226a-134">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="0226a-135">此值可能不是空白，或是只由空格所組成。</span><span class="sxs-lookup"><span data-stu-id="0226a-135">The value may not be empty or consist only of whitespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0226a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0226a-136">CommonParameters</span></span>
<span data-ttu-id="0226a-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0226a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0226a-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0226a-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0226a-139">輸入</span><span class="sxs-lookup"><span data-stu-id="0226a-139">INPUTS</span></span>

### <span data-ttu-id="0226a-140">所有</span><span class="sxs-lookup"><span data-stu-id="0226a-140">None</span></span>
<span data-ttu-id="0226a-141">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="0226a-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0226a-142">輸出</span><span class="sxs-lookup"><span data-stu-id="0226a-142">OUTPUTS</span></span>

### <span data-ttu-id="0226a-143">ServiceManagement. PsApiManagementProperty （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="0226a-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="0226a-144">筆記</span><span class="sxs-lookup"><span data-stu-id="0226a-144">NOTES</span></span>

## <span data-ttu-id="0226a-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="0226a-145">RELATED LINKS</span></span>

[<span data-ttu-id="0226a-146">移除-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="0226a-146">Remove-AzureRmApiManagementProperty</span></span>](./Remove-AzureRmApiManagementProperty.md)

[<span data-ttu-id="0226a-147">Set-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="0226a-147">Set-AzureRmApiManagementProperty</span></span>](./Set-AzureRmApiManagementProperty.md)


