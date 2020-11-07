---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F0BDB0EE-1F26-450D-9C68-34C79CE8F778
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementuserfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUserFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUserFromGroup.md
ms.openlocfilehash: 20c6894f91e92c6f70f5f753d26fe4d76a391e70
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93788806"
---
# <span data-ttu-id="fe649-101">Remove-AzApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="fe649-101">Remove-AzApiManagementUserFromGroup</span></span>

## <span data-ttu-id="fe649-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fe649-102">SYNOPSIS</span></span>
<span data-ttu-id="fe649-103">從群組中移除使用者。</span><span class="sxs-lookup"><span data-stu-id="fe649-103">Removes a user from a group.</span></span>

## <span data-ttu-id="fe649-104">句法</span><span class="sxs-lookup"><span data-stu-id="fe649-104">SYNTAX</span></span>

```
Remove-AzApiManagementUserFromGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe649-105">說明</span><span class="sxs-lookup"><span data-stu-id="fe649-105">DESCRIPTION</span></span>
<span data-ttu-id="fe649-106">**AzApiManagementUserFromGroup** Cmdlet 會從現有的群組中移除使用者。</span><span class="sxs-lookup"><span data-stu-id="fe649-106">The **Remove-AzApiManagementUserFromGroup** cmdlet removes a user from an existing group.</span></span>

## <span data-ttu-id="fe649-107">示例</span><span class="sxs-lookup"><span data-stu-id="fe649-107">EXAMPLES</span></span>

### <span data-ttu-id="fe649-108">範例1：從群組中移除使用者</span><span class="sxs-lookup"><span data-stu-id="fe649-108">Example 1: Remove a user from a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementUserFromGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="fe649-109">這個命令會從群組中移除使用者。</span><span class="sxs-lookup"><span data-stu-id="fe649-109">This command removes a user from a group.</span></span>

## <span data-ttu-id="fe649-110">參數</span><span class="sxs-lookup"><span data-stu-id="fe649-110">PARAMETERS</span></span>

### <span data-ttu-id="fe649-111">-內容</span><span class="sxs-lookup"><span data-stu-id="fe649-111">-Context</span></span>
<span data-ttu-id="fe649-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="fe649-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="fe649-113">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="fe649-113">This parameter is required.</span></span>

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

### <span data-ttu-id="fe649-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe649-114">-DefaultProfile</span></span>
<span data-ttu-id="fe649-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fe649-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe649-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="fe649-116">-GroupId</span></span>
<span data-ttu-id="fe649-117">指定要移除使用者的群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="fe649-117">Specifies the ID of the group from which to remove a user.</span></span>

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

### <span data-ttu-id="fe649-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fe649-118">-PassThru</span></span>
<span data-ttu-id="fe649-119">指示這個 Cmdlet 會傳回 $True 的值（如果它成功的話），否則傳回 $False 的值。</span><span class="sxs-lookup"><span data-stu-id="fe649-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="fe649-120">-UserId</span><span class="sxs-lookup"><span data-stu-id="fe649-120">-UserId</span></span>
<span data-ttu-id="fe649-121">指定要從群組中移除的使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="fe649-121">Specifies the ID of the user to remove from the group.</span></span>

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

### <span data-ttu-id="fe649-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe649-122">CommonParameters</span></span>
<span data-ttu-id="fe649-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fe649-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe649-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fe649-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe649-125">輸入</span><span class="sxs-lookup"><span data-stu-id="fe649-125">INPUTS</span></span>

### <span data-ttu-id="fe649-126">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="fe649-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="fe649-127">System.object</span><span class="sxs-lookup"><span data-stu-id="fe649-127">System.String</span></span>

### <span data-ttu-id="fe649-128">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="fe649-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fe649-129">輸出</span><span class="sxs-lookup"><span data-stu-id="fe649-129">OUTPUTS</span></span>

### <span data-ttu-id="fe649-130">System.object</span><span class="sxs-lookup"><span data-stu-id="fe649-130">System.Boolean</span></span>

## <span data-ttu-id="fe649-131">筆記</span><span class="sxs-lookup"><span data-stu-id="fe649-131">NOTES</span></span>

## <span data-ttu-id="fe649-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="fe649-132">RELATED LINKS</span></span>

[<span data-ttu-id="fe649-133">附加 AzApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="fe649-133">Add-AzApiManagementUserToGroup</span></span>](./Add-AzApiManagementUserToGroup.md)

[<span data-ttu-id="fe649-134">AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="fe649-134">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)


