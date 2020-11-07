---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5C0C437D-7237-4B40-A254-1B55916F1C71
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProperty.md
ms.openlocfilehash: 89612136023173d2f725c8c4b286a270400f8c6a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625639"
---
# <span data-ttu-id="921a5-101">Set-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="921a5-101">Set-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="921a5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="921a5-102">SYNOPSIS</span></span>
<span data-ttu-id="921a5-103">修改 API 管理屬性。</span><span class="sxs-lookup"><span data-stu-id="921a5-103">Modifies an API Management Property.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="921a5-104">句法</span><span class="sxs-lookup"><span data-stu-id="921a5-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementProperty -Context <PsApiManagementContext> -PropertyId <String> [-Name <String>]
 [-Value <String>] [-Secret <Boolean>] [-Tag <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="921a5-105">說明</span><span class="sxs-lookup"><span data-stu-id="921a5-105">DESCRIPTION</span></span>
<span data-ttu-id="921a5-106">**AzureRmApiManagementProperty** Cmdlet 會修改 Azure API 管理屬性。</span><span class="sxs-lookup"><span data-stu-id="921a5-106">The **Set-AzureRmApiManagementProperty** cmdlet modifies an Azure API Management Property.</span></span>

## <span data-ttu-id="921a5-107">示例</span><span class="sxs-lookup"><span data-stu-id="921a5-107">EXAMPLES</span></span>

### <span data-ttu-id="921a5-108">範例1：變更屬性上的標記</span><span class="sxs-lookup"><span data-stu-id="921a5-108">Example 1: Change the tags on a property</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> Set-AzureRmApiManagementProperty -Context $apimContext -PropertyId "Property11" -Tags $Tags -PassThru
```

<span data-ttu-id="921a5-109">第一個命令會將兩個值指派給 $Tags 變數。</span><span class="sxs-lookup"><span data-stu-id="921a5-109">The first command assigns two values to the $Tags variable.</span></span>

<span data-ttu-id="921a5-110">第二個命令會修改 ID 為 Property11 的屬性。</span><span class="sxs-lookup"><span data-stu-id="921a5-110">The second command modifies the property that has the ID Property11.</span></span>
<span data-ttu-id="921a5-111">命令會將 $Tags 中的字串指定為屬性上的標記。</span><span class="sxs-lookup"><span data-stu-id="921a5-111">The command assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="921a5-112">範例2：修改屬性以有機密值</span><span class="sxs-lookup"><span data-stu-id="921a5-112">Example 2: Modify a property to have a secret value</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementProperty -Context $apimContext -PropertyId "Property12" -Secret $True -PassThru
```

<span data-ttu-id="921a5-113">這個命令會將屬性變更為已加密。</span><span class="sxs-lookup"><span data-stu-id="921a5-113">This command changes the property to be Encrypted.</span></span>

## <span data-ttu-id="921a5-114">參數</span><span class="sxs-lookup"><span data-stu-id="921a5-114">PARAMETERS</span></span>

### <span data-ttu-id="921a5-115">-內容</span><span class="sxs-lookup"><span data-stu-id="921a5-115">-Context</span></span>
<span data-ttu-id="921a5-116">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="921a5-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="921a5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="921a5-117">-DefaultProfile</span></span>
<span data-ttu-id="921a5-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="921a5-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="921a5-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="921a5-119">-Name</span></span>
<span data-ttu-id="921a5-120">指定屬性的名稱。</span><span class="sxs-lookup"><span data-stu-id="921a5-120">Specifies the name of the property.</span></span>
<span data-ttu-id="921a5-121">最大長度為100個字元。</span><span class="sxs-lookup"><span data-stu-id="921a5-121">Maximum length is 100 characters.</span></span>
<span data-ttu-id="921a5-122">名稱只包含字母、數位、句點、破折號及底線字元。</span><span class="sxs-lookup"><span data-stu-id="921a5-122">Names contain only letters, digits, period, dash, and underscore characters.</span></span>

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

### <span data-ttu-id="921a5-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="921a5-123">-PassThru</span></span>
<span data-ttu-id="921a5-124">指示這個 Cmdlet 會傳回這個 Cmdlet 修改的 **PsApiManagementProperty** 。</span><span class="sxs-lookup"><span data-stu-id="921a5-124">Indicates that this cmdlet returns the **PsApiManagementProperty** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="921a5-125">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="921a5-125">-PropertyId</span></span>
<span data-ttu-id="921a5-126">指定此 Cmdlet 所修改之屬性的識別碼。</span><span class="sxs-lookup"><span data-stu-id="921a5-126">Specifies an ID of the property that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="921a5-127">密碼</span><span class="sxs-lookup"><span data-stu-id="921a5-127">-Secret</span></span>
<span data-ttu-id="921a5-128">表示屬性值是一個機密，應該經過加密。</span><span class="sxs-lookup"><span data-stu-id="921a5-128">Indicates that the property value is a secret and should be encrypted.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="921a5-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="921a5-129">-Tag</span></span>
<span data-ttu-id="921a5-130">與屬性相關聯的標記。</span><span class="sxs-lookup"><span data-stu-id="921a5-130">Tags associated with a property.</span></span> <span data-ttu-id="921a5-131">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="921a5-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="921a5-132">-值</span><span class="sxs-lookup"><span data-stu-id="921a5-132">-Value</span></span>
<span data-ttu-id="921a5-133">指定屬性的值。</span><span class="sxs-lookup"><span data-stu-id="921a5-133">Specifies a value for the property.</span></span>
<span data-ttu-id="921a5-134">這個值可以包含原則運算式。</span><span class="sxs-lookup"><span data-stu-id="921a5-134">This value can contain policy expressions.</span></span>
<span data-ttu-id="921a5-135">最大長度為1000個字元。</span><span class="sxs-lookup"><span data-stu-id="921a5-135">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="921a5-136">此值可能不是空白，或是只由空格所組成。</span><span class="sxs-lookup"><span data-stu-id="921a5-136">The value may not be empty or consist only of whitespace.</span></span>

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

### <span data-ttu-id="921a5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="921a5-137">CommonParameters</span></span>
<span data-ttu-id="921a5-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="921a5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="921a5-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="921a5-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="921a5-140">輸入</span><span class="sxs-lookup"><span data-stu-id="921a5-140">INPUTS</span></span>

### <span data-ttu-id="921a5-141">所有</span><span class="sxs-lookup"><span data-stu-id="921a5-141">None</span></span>
<span data-ttu-id="921a5-142">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="921a5-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="921a5-143">輸出</span><span class="sxs-lookup"><span data-stu-id="921a5-143">OUTPUTS</span></span>

### <span data-ttu-id="921a5-144">ServiceManagement. PsApiManagementProperty （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="921a5-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="921a5-145">筆記</span><span class="sxs-lookup"><span data-stu-id="921a5-145">NOTES</span></span>

## <span data-ttu-id="921a5-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="921a5-146">RELATED LINKS</span></span>

[<span data-ttu-id="921a5-147">AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="921a5-147">Get-AzureRmApiManagementProperty</span></span>](./Get-AzureRmApiManagementProperty.md)

[<span data-ttu-id="921a5-148">新-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="921a5-148">New-AzureRmApiManagementProperty</span></span>](./New-AzureRmApiManagementProperty.md)

[<span data-ttu-id="921a5-149">移除-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="921a5-149">Remove-AzureRmApiManagementProperty</span></span>](./Remove-AzureRmApiManagementProperty.md)


