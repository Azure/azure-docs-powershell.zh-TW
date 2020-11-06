---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5C0C437D-7237-4B40-A254-1B55916F1C71
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProperty.md
ms.openlocfilehash: 162cdc0fdad8a9f3db33ff928a3524f942be16c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445795"
---
# <span data-ttu-id="70fd4-101">Set-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="70fd4-101">Set-AzureRmApiManagementProperty</span></span>

## <span data-ttu-id="70fd4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="70fd4-102">SYNOPSIS</span></span>
<span data-ttu-id="70fd4-103">修改 API 管理屬性。</span><span class="sxs-lookup"><span data-stu-id="70fd4-103">Modifies an API Management Property.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70fd4-104">句法</span><span class="sxs-lookup"><span data-stu-id="70fd4-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementProperty -Context <PsApiManagementContext> -PropertyId <String> [-Name <String>]
 [-Value <String>] [-Secret <Boolean>] [-Tag <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="70fd4-105">說明</span><span class="sxs-lookup"><span data-stu-id="70fd4-105">DESCRIPTION</span></span>
<span data-ttu-id="70fd4-106">**AzureRmApiManagementProperty** Cmdlet 會修改 Azure API 管理屬性。</span><span class="sxs-lookup"><span data-stu-id="70fd4-106">The **Set-AzureRmApiManagementProperty** cmdlet modifies an Azure API Management Property.</span></span>

## <span data-ttu-id="70fd4-107">示例</span><span class="sxs-lookup"><span data-stu-id="70fd4-107">EXAMPLES</span></span>

### <span data-ttu-id="70fd4-108">範例1：變更屬性上的標記</span><span class="sxs-lookup"><span data-stu-id="70fd4-108">Example 1: Change the tags on a property</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$Tags = 'sdk', 'powershell'
PS C:\> Set-AzureRmApiManagementProperty -Context $apimContext -PropertyId "Property11" -Tags $Tags -PassThru
```

<span data-ttu-id="70fd4-109">第一個命令會將兩個值指派給 $Tags 變數。</span><span class="sxs-lookup"><span data-stu-id="70fd4-109">The first command assigns two values to the $Tags variable.</span></span>
<span data-ttu-id="70fd4-110">第二個命令會修改 ID 為 Property11 的屬性。</span><span class="sxs-lookup"><span data-stu-id="70fd4-110">The second command modifies the property that has the ID Property11.</span></span>
<span data-ttu-id="70fd4-111">命令會將 $Tags 中的字串指定為屬性上的標記。</span><span class="sxs-lookup"><span data-stu-id="70fd4-111">The command assigns the strings in $Tags as tags on the property.</span></span>

### <span data-ttu-id="70fd4-112">範例2：修改屬性以有機密值</span><span class="sxs-lookup"><span data-stu-id="70fd4-112">Example 2: Modify a property to have a secret value</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementProperty -Context $apimContext -PropertyId "Property12" -Secret $True -PassThru
```

<span data-ttu-id="70fd4-113">這個命令會將屬性變更為已加密。</span><span class="sxs-lookup"><span data-stu-id="70fd4-113">This command changes the property to be Encrypted.</span></span>

## <span data-ttu-id="70fd4-114">參數</span><span class="sxs-lookup"><span data-stu-id="70fd4-114">PARAMETERS</span></span>

### <span data-ttu-id="70fd4-115">-內容</span><span class="sxs-lookup"><span data-stu-id="70fd4-115">-Context</span></span>
<span data-ttu-id="70fd4-116">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="70fd4-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="70fd4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70fd4-117">-DefaultProfile</span></span>
<span data-ttu-id="70fd4-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="70fd4-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70fd4-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="70fd4-119">-Name</span></span>
<span data-ttu-id="70fd4-120">指定屬性的名稱。</span><span class="sxs-lookup"><span data-stu-id="70fd4-120">Specifies the name of the property.</span></span>
<span data-ttu-id="70fd4-121">最大長度為100個字元。</span><span class="sxs-lookup"><span data-stu-id="70fd4-121">Maximum length is 100 characters.</span></span>
<span data-ttu-id="70fd4-122">名稱只包含字母、數位、句點、破折號及底線字元。</span><span class="sxs-lookup"><span data-stu-id="70fd4-122">Names contain only letters, digits, period, dash, and underscore characters.</span></span>

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

### <span data-ttu-id="70fd4-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="70fd4-123">-PassThru</span></span>
<span data-ttu-id="70fd4-124">指示這個 Cmdlet 會傳回這個 Cmdlet 修改的 **PsApiManagementProperty** 。</span><span class="sxs-lookup"><span data-stu-id="70fd4-124">Indicates that this cmdlet returns the **PsApiManagementProperty** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="70fd4-125">-PropertyId</span><span class="sxs-lookup"><span data-stu-id="70fd4-125">-PropertyId</span></span>
<span data-ttu-id="70fd4-126">指定此 Cmdlet 所修改之屬性的識別碼。</span><span class="sxs-lookup"><span data-stu-id="70fd4-126">Specifies an ID of the property that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="70fd4-127">密碼</span><span class="sxs-lookup"><span data-stu-id="70fd4-127">-Secret</span></span>
<span data-ttu-id="70fd4-128">表示屬性值是一個機密，應該經過加密。</span><span class="sxs-lookup"><span data-stu-id="70fd4-128">Indicates that the property value is a secret and should be encrypted.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70fd4-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="70fd4-129">-Tag</span></span>
<span data-ttu-id="70fd4-130">與屬性相關聯的標記。</span><span class="sxs-lookup"><span data-stu-id="70fd4-130">Tags associated with a property.</span></span> <span data-ttu-id="70fd4-131">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="70fd4-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="70fd4-132">-值</span><span class="sxs-lookup"><span data-stu-id="70fd4-132">-Value</span></span>
<span data-ttu-id="70fd4-133">指定屬性的值。</span><span class="sxs-lookup"><span data-stu-id="70fd4-133">Specifies a value for the property.</span></span>
<span data-ttu-id="70fd4-134">這個值可以包含原則運算式。</span><span class="sxs-lookup"><span data-stu-id="70fd4-134">This value can contain policy expressions.</span></span>
<span data-ttu-id="70fd4-135">最大長度為1000個字元。</span><span class="sxs-lookup"><span data-stu-id="70fd4-135">Maximum length is 1000 characters.</span></span>
<span data-ttu-id="70fd4-136">此值可能不是空白，或是只由空格所組成。</span><span class="sxs-lookup"><span data-stu-id="70fd4-136">The value may not be empty or consist only of whitespace.</span></span>

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

### <span data-ttu-id="70fd4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70fd4-137">CommonParameters</span></span>
<span data-ttu-id="70fd4-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="70fd4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70fd4-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="70fd4-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70fd4-140">輸入</span><span class="sxs-lookup"><span data-stu-id="70fd4-140">INPUTS</span></span>

### <span data-ttu-id="70fd4-141">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="70fd4-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="70fd4-142">System.object</span><span class="sxs-lookup"><span data-stu-id="70fd4-142">System.String</span></span>

### <span data-ttu-id="70fd4-143">系統為 Nullable "1 [[System.object，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="70fd4-143">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="70fd4-144">System.object []</span><span class="sxs-lookup"><span data-stu-id="70fd4-144">System.String[]</span></span>

### <span data-ttu-id="70fd4-145">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="70fd4-145">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="70fd4-146">輸出</span><span class="sxs-lookup"><span data-stu-id="70fd4-146">OUTPUTS</span></span>

### <span data-ttu-id="70fd4-147">ServiceManagement. PsApiManagementProperty （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="70fd4-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProperty</span></span>

## <span data-ttu-id="70fd4-148">筆記</span><span class="sxs-lookup"><span data-stu-id="70fd4-148">NOTES</span></span>

## <span data-ttu-id="70fd4-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="70fd4-149">RELATED LINKS</span></span>

[<span data-ttu-id="70fd4-150">AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="70fd4-150">Get-AzureRmApiManagementProperty</span></span>](./Get-AzureRmApiManagementProperty.md)

[<span data-ttu-id="70fd4-151">新-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="70fd4-151">New-AzureRmApiManagementProperty</span></span>](./New-AzureRmApiManagementProperty.md)

[<span data-ttu-id="70fd4-152">移除-AzureRmApiManagementProperty</span><span class="sxs-lookup"><span data-stu-id="70fd4-152">Remove-AzureRmApiManagementProperty</span></span>](./Remove-AzureRmApiManagementProperty.md)


