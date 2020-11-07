---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 8C014335-9622-4F2E-A163-4B0C84531506
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/add-azurermapimanagementusertogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementUserToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementUserToGroup.md
ms.openlocfilehash: 300c99926ae7f58a6bf53ba49f3b5b86f243e150
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625040"
---
# <span data-ttu-id="72ec5-101">Add-AzureRmApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="72ec5-101">Add-AzureRmApiManagementUserToGroup</span></span>

## <span data-ttu-id="72ec5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="72ec5-102">SYNOPSIS</span></span>
<span data-ttu-id="72ec5-103">將使用者新增至群組。</span><span class="sxs-lookup"><span data-stu-id="72ec5-103">Adds a user to a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72ec5-104">句法</span><span class="sxs-lookup"><span data-stu-id="72ec5-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementUserToGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72ec5-105">說明</span><span class="sxs-lookup"><span data-stu-id="72ec5-105">DESCRIPTION</span></span>
<span data-ttu-id="72ec5-106">**AzureRmApiManagementUserToGroup** Cmdlet 會將使用者新增至群組。</span><span class="sxs-lookup"><span data-stu-id="72ec5-106">The **Add-AzureRmApiManagementUserToGroup** cmdlet adds a user to a group.</span></span>

## <span data-ttu-id="72ec5-107">示例</span><span class="sxs-lookup"><span data-stu-id="72ec5-107">EXAMPLES</span></span>

### <span data-ttu-id="72ec5-108">範例1：將使用者新增至群組</span><span class="sxs-lookup"><span data-stu-id="72ec5-108">Example 1: Add a user to a group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzureRmApiManagementUserToGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="72ec5-109">這個命令會將現有的使用者新增至現有的群組。</span><span class="sxs-lookup"><span data-stu-id="72ec5-109">This command adds an existing user to an existing group.</span></span>

## <span data-ttu-id="72ec5-110">參數</span><span class="sxs-lookup"><span data-stu-id="72ec5-110">PARAMETERS</span></span>

### <span data-ttu-id="72ec5-111">-內容</span><span class="sxs-lookup"><span data-stu-id="72ec5-111">-Context</span></span>
<span data-ttu-id="72ec5-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="72ec5-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="72ec5-113">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="72ec5-113">This parameter is required.</span></span>

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

### <span data-ttu-id="72ec5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72ec5-114">-DefaultProfile</span></span>
<span data-ttu-id="72ec5-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="72ec5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="72ec5-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="72ec5-116">-GroupId</span></span>
<span data-ttu-id="72ec5-117">指定群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="72ec5-117">Specifies the group ID.</span></span>
<span data-ttu-id="72ec5-118">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="72ec5-118">This parameter is required.</span></span>

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

### <span data-ttu-id="72ec5-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="72ec5-119">-PassThru</span></span>
<span data-ttu-id="72ec5-120">passthru</span><span class="sxs-lookup"><span data-stu-id="72ec5-120">passthru</span></span>

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

### <span data-ttu-id="72ec5-121">-UserId</span><span class="sxs-lookup"><span data-stu-id="72ec5-121">-UserId</span></span>
<span data-ttu-id="72ec5-122">指定使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="72ec5-122">Specifies the user ID.</span></span>
<span data-ttu-id="72ec5-123">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="72ec5-123">This parameter is required.</span></span>

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

### <span data-ttu-id="72ec5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72ec5-124">CommonParameters</span></span>
<span data-ttu-id="72ec5-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="72ec5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72ec5-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="72ec5-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72ec5-127">輸入</span><span class="sxs-lookup"><span data-stu-id="72ec5-127">INPUTS</span></span>

### <span data-ttu-id="72ec5-128">所有</span><span class="sxs-lookup"><span data-stu-id="72ec5-128">None</span></span>
<span data-ttu-id="72ec5-129">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="72ec5-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="72ec5-130">輸出</span><span class="sxs-lookup"><span data-stu-id="72ec5-130">OUTPUTS</span></span>

### <span data-ttu-id="72ec5-131">布林值</span><span class="sxs-lookup"><span data-stu-id="72ec5-131">Boolean</span></span>

## <span data-ttu-id="72ec5-132">筆記</span><span class="sxs-lookup"><span data-stu-id="72ec5-132">NOTES</span></span>

## <span data-ttu-id="72ec5-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="72ec5-133">RELATED LINKS</span></span>

[<span data-ttu-id="72ec5-134">AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="72ec5-134">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="72ec5-135">移除-AzureRmApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="72ec5-135">Remove-AzureRmApiManagementUserFromGroup</span></span>](./Remove-AzureRmApiManagementUserFromGroup.md)


