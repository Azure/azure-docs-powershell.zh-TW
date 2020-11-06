---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: F0BDB0EE-1F26-450D-9C68-34C79CE8F778
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementuserfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUserFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUserFromGroup.md
ms.openlocfilehash: bdcbac04d621319ac3837f1efaef52018e0f4eba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457500"
---
# <span data-ttu-id="ded4f-101">Remove-AzureRmApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="ded4f-101">Remove-AzureRmApiManagementUserFromGroup</span></span>

## <span data-ttu-id="ded4f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ded4f-102">SYNOPSIS</span></span>
<span data-ttu-id="ded4f-103">從群組中移除使用者。</span><span class="sxs-lookup"><span data-stu-id="ded4f-103">Removes a user from a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ded4f-104">句法</span><span class="sxs-lookup"><span data-stu-id="ded4f-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementUserFromGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ded4f-105">說明</span><span class="sxs-lookup"><span data-stu-id="ded4f-105">DESCRIPTION</span></span>
<span data-ttu-id="ded4f-106">**AzureRmApiManagementUserFromGroup** Cmdlet 會從現有的群組中移除使用者。</span><span class="sxs-lookup"><span data-stu-id="ded4f-106">The **Remove-AzureRmApiManagementUserFromGroup** cmdlet removes a user from an existing group.</span></span>

## <span data-ttu-id="ded4f-107">示例</span><span class="sxs-lookup"><span data-stu-id="ded4f-107">EXAMPLES</span></span>

### <span data-ttu-id="ded4f-108">範例1：從群組中移除使用者</span><span class="sxs-lookup"><span data-stu-id="ded4f-108">Example 1: Remove a user from a group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementUserFromGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="ded4f-109">這個命令會從群組中移除使用者。</span><span class="sxs-lookup"><span data-stu-id="ded4f-109">This command removes a user from a group.</span></span>

## <span data-ttu-id="ded4f-110">參數</span><span class="sxs-lookup"><span data-stu-id="ded4f-110">PARAMETERS</span></span>

### <span data-ttu-id="ded4f-111">-內容</span><span class="sxs-lookup"><span data-stu-id="ded4f-111">-Context</span></span>
<span data-ttu-id="ded4f-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="ded4f-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="ded4f-113">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="ded4f-113">This parameter is required.</span></span>

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

### <span data-ttu-id="ded4f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ded4f-114">-DefaultProfile</span></span>
<span data-ttu-id="ded4f-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ded4f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="ded4f-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="ded4f-116">-GroupId</span></span>
<span data-ttu-id="ded4f-117">指定要移除使用者的群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="ded4f-117">Specifies the ID of the group from which to remove a user.</span></span>

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

### <span data-ttu-id="ded4f-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ded4f-118">-PassThru</span></span>
<span data-ttu-id="ded4f-119">指示這個 Cmdlet 會傳回 $True 的值（如果它成功的話），否則傳回 $False 的值。</span><span class="sxs-lookup"><span data-stu-id="ded4f-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="ded4f-120">-UserId</span><span class="sxs-lookup"><span data-stu-id="ded4f-120">-UserId</span></span>
<span data-ttu-id="ded4f-121">指定要從群組中移除的使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="ded4f-121">Specifies the ID of the user to remove from the group.</span></span>

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

### <span data-ttu-id="ded4f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ded4f-122">CommonParameters</span></span>
<span data-ttu-id="ded4f-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ded4f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ded4f-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ded4f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ded4f-125">輸入</span><span class="sxs-lookup"><span data-stu-id="ded4f-125">INPUTS</span></span>

### <span data-ttu-id="ded4f-126">所有</span><span class="sxs-lookup"><span data-stu-id="ded4f-126">None</span></span>
<span data-ttu-id="ded4f-127">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="ded4f-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ded4f-128">輸出</span><span class="sxs-lookup"><span data-stu-id="ded4f-128">OUTPUTS</span></span>

### <span data-ttu-id="ded4f-129">System.object</span><span class="sxs-lookup"><span data-stu-id="ded4f-129">System.Boolean</span></span>

## <span data-ttu-id="ded4f-130">筆記</span><span class="sxs-lookup"><span data-stu-id="ded4f-130">NOTES</span></span>

## <span data-ttu-id="ded4f-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="ded4f-131">RELATED LINKS</span></span>

[<span data-ttu-id="ded4f-132">附加 AzureRmApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="ded4f-132">Add-AzureRmApiManagementUserToGroup</span></span>](./Add-AzureRmApiManagementUserToGroup.md)

[<span data-ttu-id="ded4f-133">AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="ded4f-133">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)


