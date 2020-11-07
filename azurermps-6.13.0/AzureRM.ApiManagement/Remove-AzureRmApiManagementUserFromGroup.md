---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: F0BDB0EE-1F26-450D-9C68-34C79CE8F778
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementuserfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUserFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUserFromGroup.md
ms.openlocfilehash: abf9cab8e7e832a6221a25aff40f4d7b7ae55d58
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624951"
---
# <span data-ttu-id="e34f4-101">Remove-AzureRmApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="e34f4-101">Remove-AzureRmApiManagementUserFromGroup</span></span>

## <span data-ttu-id="e34f4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e34f4-102">SYNOPSIS</span></span>
<span data-ttu-id="e34f4-103">從群組中移除使用者。</span><span class="sxs-lookup"><span data-stu-id="e34f4-103">Removes a user from a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e34f4-104">句法</span><span class="sxs-lookup"><span data-stu-id="e34f4-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementUserFromGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e34f4-105">說明</span><span class="sxs-lookup"><span data-stu-id="e34f4-105">DESCRIPTION</span></span>
<span data-ttu-id="e34f4-106">**AzureRmApiManagementUserFromGroup** Cmdlet 會從現有的群組中移除使用者。</span><span class="sxs-lookup"><span data-stu-id="e34f4-106">The **Remove-AzureRmApiManagementUserFromGroup** cmdlet removes a user from an existing group.</span></span>

## <span data-ttu-id="e34f4-107">示例</span><span class="sxs-lookup"><span data-stu-id="e34f4-107">EXAMPLES</span></span>

### <span data-ttu-id="e34f4-108">範例1：從群組中移除使用者</span><span class="sxs-lookup"><span data-stu-id="e34f4-108">Example 1: Remove a user from a group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementUserFromGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="e34f4-109">這個命令會從群組中移除使用者。</span><span class="sxs-lookup"><span data-stu-id="e34f4-109">This command removes a user from a group.</span></span>

## <span data-ttu-id="e34f4-110">參數</span><span class="sxs-lookup"><span data-stu-id="e34f4-110">PARAMETERS</span></span>

### <span data-ttu-id="e34f4-111">-內容</span><span class="sxs-lookup"><span data-stu-id="e34f4-111">-Context</span></span>
<span data-ttu-id="e34f4-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="e34f4-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="e34f4-113">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="e34f4-113">This parameter is required.</span></span>

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

### <span data-ttu-id="e34f4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e34f4-114">-DefaultProfile</span></span>
<span data-ttu-id="e34f4-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e34f4-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e34f4-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="e34f4-116">-GroupId</span></span>
<span data-ttu-id="e34f4-117">指定要移除使用者的群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="e34f4-117">Specifies the ID of the group from which to remove a user.</span></span>

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

### <span data-ttu-id="e34f4-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e34f4-118">-PassThru</span></span>
<span data-ttu-id="e34f4-119">指示這個 Cmdlet 會傳回 $True 的值（如果它成功的話），否則傳回 $False 的值。</span><span class="sxs-lookup"><span data-stu-id="e34f4-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="e34f4-120">-UserId</span><span class="sxs-lookup"><span data-stu-id="e34f4-120">-UserId</span></span>
<span data-ttu-id="e34f4-121">指定要從群組中移除的使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="e34f4-121">Specifies the ID of the user to remove from the group.</span></span>

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

### <span data-ttu-id="e34f4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e34f4-122">CommonParameters</span></span>
<span data-ttu-id="e34f4-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e34f4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e34f4-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e34f4-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e34f4-125">輸入</span><span class="sxs-lookup"><span data-stu-id="e34f4-125">INPUTS</span></span>

### <span data-ttu-id="e34f4-126">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="e34f4-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e34f4-127">System.object</span><span class="sxs-lookup"><span data-stu-id="e34f4-127">System.String</span></span>

### <span data-ttu-id="e34f4-128">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="e34f4-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e34f4-129">輸出</span><span class="sxs-lookup"><span data-stu-id="e34f4-129">OUTPUTS</span></span>

### <span data-ttu-id="e34f4-130">System.object</span><span class="sxs-lookup"><span data-stu-id="e34f4-130">System.Boolean</span></span>

## <span data-ttu-id="e34f4-131">筆記</span><span class="sxs-lookup"><span data-stu-id="e34f4-131">NOTES</span></span>

## <span data-ttu-id="e34f4-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="e34f4-132">RELATED LINKS</span></span>

[<span data-ttu-id="e34f4-133">附加 AzureRmApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="e34f4-133">Add-AzureRmApiManagementUserToGroup</span></span>](./Add-AzureRmApiManagementUserToGroup.md)

[<span data-ttu-id="e34f4-134">AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="e34f4-134">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)


