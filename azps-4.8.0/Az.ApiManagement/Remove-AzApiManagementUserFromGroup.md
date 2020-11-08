---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F0BDB0EE-1F26-450D-9C68-34C79CE8F778
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementuserfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUserFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUserFromGroup.md
ms.openlocfilehash: 220af172efa397de2fc0fafa7597c2b6e29dae60
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126602"
---
# <span data-ttu-id="4b273-101">Remove-AzApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="4b273-101">Remove-AzApiManagementUserFromGroup</span></span>

## <span data-ttu-id="4b273-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4b273-102">SYNOPSIS</span></span>
<span data-ttu-id="4b273-103">從群組中移除使用者。</span><span class="sxs-lookup"><span data-stu-id="4b273-103">Removes a user from a group.</span></span>

## <span data-ttu-id="4b273-104">句法</span><span class="sxs-lookup"><span data-stu-id="4b273-104">SYNTAX</span></span>

```
Remove-AzApiManagementUserFromGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b273-105">說明</span><span class="sxs-lookup"><span data-stu-id="4b273-105">DESCRIPTION</span></span>
<span data-ttu-id="4b273-106">**AzApiManagementUserFromGroup** Cmdlet 會從現有的群組中移除使用者。</span><span class="sxs-lookup"><span data-stu-id="4b273-106">The **Remove-AzApiManagementUserFromGroup** cmdlet removes a user from an existing group.</span></span>

## <span data-ttu-id="4b273-107">示例</span><span class="sxs-lookup"><span data-stu-id="4b273-107">EXAMPLES</span></span>

### <span data-ttu-id="4b273-108">範例1：從群組中移除使用者</span><span class="sxs-lookup"><span data-stu-id="4b273-108">Example 1: Remove a user from a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementUserFromGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="4b273-109">這個命令會從群組中移除使用者。</span><span class="sxs-lookup"><span data-stu-id="4b273-109">This command removes a user from a group.</span></span>

## <span data-ttu-id="4b273-110">參數</span><span class="sxs-lookup"><span data-stu-id="4b273-110">PARAMETERS</span></span>

### <span data-ttu-id="4b273-111">-內容</span><span class="sxs-lookup"><span data-stu-id="4b273-111">-Context</span></span>
<span data-ttu-id="4b273-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="4b273-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="4b273-113">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="4b273-113">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4b273-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b273-114">-DefaultProfile</span></span>
<span data-ttu-id="4b273-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4b273-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b273-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="4b273-116">-GroupId</span></span>
<span data-ttu-id="4b273-117">指定要移除使用者的群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="4b273-117">Specifies the ID of the group from which to remove a user.</span></span>

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

### <span data-ttu-id="4b273-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4b273-118">-PassThru</span></span>
<span data-ttu-id="4b273-119">指示這個 Cmdlet 會傳回 $True 的值（如果它成功的話），否則傳回 $False 的值。</span><span class="sxs-lookup"><span data-stu-id="4b273-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="4b273-120">-UserId</span><span class="sxs-lookup"><span data-stu-id="4b273-120">-UserId</span></span>
<span data-ttu-id="4b273-121">指定要從群組中移除的使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="4b273-121">Specifies the ID of the user to remove from the group.</span></span>

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

### <span data-ttu-id="4b273-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b273-122">CommonParameters</span></span>
<span data-ttu-id="4b273-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4b273-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b273-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4b273-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b273-125">輸入</span><span class="sxs-lookup"><span data-stu-id="4b273-125">INPUTS</span></span>

### <span data-ttu-id="4b273-126">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="4b273-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4b273-127">System.object</span><span class="sxs-lookup"><span data-stu-id="4b273-127">System.String</span></span>

### <span data-ttu-id="4b273-128">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="4b273-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4b273-129">輸出</span><span class="sxs-lookup"><span data-stu-id="4b273-129">OUTPUTS</span></span>

### <span data-ttu-id="4b273-130">System.object</span><span class="sxs-lookup"><span data-stu-id="4b273-130">System.Boolean</span></span>

## <span data-ttu-id="4b273-131">筆記</span><span class="sxs-lookup"><span data-stu-id="4b273-131">NOTES</span></span>

## <span data-ttu-id="4b273-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="4b273-132">RELATED LINKS</span></span>

[<span data-ttu-id="4b273-133">附加 AzApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="4b273-133">Add-AzApiManagementUserToGroup</span></span>](./Add-AzApiManagementUserToGroup.md)

[<span data-ttu-id="4b273-134">AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="4b273-134">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)


